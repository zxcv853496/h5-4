<template>
  <div id="app">
    <div class="topcover" :class="{'active': !active}">
      <div>
        <img class="back" src="/img/mainpage/main-back.webp" alt="">
        <img class="back" src="/img/mainpage/back-animation.webp" alt="">
        <img class="back" src="/img/mainpage/back-yellow.webp" alt="">
      </div>
    </div>
    <div class="basic-cover"
    :class="{'touch':touch}">
      <div class="label">{{ label }}</div>
      <div class="finger-container">
        <img class="finger" src="/img/topcover/finger.png" alt=""
        @touchstart='touch = true'
        v-on:click="isMobile">
        <img class="scan" src="/img/topcover/scan.png" alt=""
        :class="{'touch':touch}">
      </div>
    </div>
    <audio id="audio" autoplay>
        <source :src="require('@/assets/music/GetUp by RazBurg Artlist.wav')" type="audio/mpeg">
    </audio>
    <button class="btn-music" id="btn-music"
    :class="{'paused':btnPuased}"
    @click="audioAutoPlay">
      <i class="material-icons md-18">music_note</i>
    </button>
    <div class="arrow-up">
      <i class="fas fa-angle-double-up"></i>
    </div>
    <full-page :options="options" ref="fullpage"  >
      <div class="section"  >
        <Mainpage :active="active"/>
      </div>  
      <div class="section" >
        <Twopage :active="active"/>
      </div>     
      <div class="section" >
        <Threepage :active="active"/>
      </div>         
      <div class="section" >
        <Fourpage :active="active"/>
      </div>      
      <div class="section" >
        <Fivepage :active="active"/>
      </div>      
      <div class="section" >
        <Sixpage :active="active"/>
      </div>     
      <div class="section" >
        <Sevenpage :active="active"/>
      </div> 
      <div class="section" >
        <Eightpage :active="active"/>
      </div>     
    </full-page>
  </div>
</template>

<script>
import './assets/css/app.scss'
import Mainpage from './components/mainpage/index'
import Twopage from './components/twopage/index'
import Threepage from './components/threepage/index'
import Fourpage from './components/fourpage/index'
import Fivepage from './components/fivepage/index'
import Sixpage from './components/sixpage/index'
import Sevenpage from './components/sevenpage/index'
import Eightpage from './components/eightpage/index'

export default {
  name: 'App',
  components: {
    Mainpage,
    Twopage,
    Threepage,
    Fourpage,
    Fivepage,
    Sixpage,
    Sevenpage,
    Eightpage,
  },
  data() {
    return{
      mobilAudio:false,
      btnPuased:true,
      touch:false,
      active:false,
      label:'',
      options: {
        licenseKey: "OPEN-SOURCE-GPLV3-LICENSE",
        //是否顯示導航，預設為false
        navigation: true,
        
        //頁面滾動速度
        scrollingSpeed: 700,
        //動畫
        controlArrows: true,
        loopBottom:true,
        loopTop:true ,
        onLeave: this.movePage,
        afterLoad: this.movePageAfter,
      },
    }
  },
  watch:{
    touch:{
      handler: function(){
        this.label = '掃描中...'
        var audio = document.getElementById('audio');
        audio.play();
        if (!audio.paused){
          this.btnPuased = false;
        }
        setTimeout(()=> {
          this.label ='掃描成功!'
          this.movePageAfter()
        },1000)
      }
    },
  },
  methods:{
    pctouch(){
      var width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
      if (width > 1050){
        this.touch = true
      }
      else{
        console.log('手機端')
      }
    },
    isMobile(){
      let flag = navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|WebOS|Symbian|Windows Phone)/i)
      if (flag){
        console.log('手機端')
      }
      else{
        this.touch = true
      }
    },
    audioAutoPlay(){
      var audio = document.getElementById('audio');
      if (audio.paused){
        audio.play();
        this.btnPuased = false;
      }
      else {
        audio.pause();
        this.btnPuased = true;
      }
    },
    movePage(){
      
      this.active =! this.active
      console.log(this.active)
      
    },
    movePageAfter(){
      if (this.touch != false){
        this.active =! this.active
        
        console.log(this.active)
      }
    },
  }
}
</script>


