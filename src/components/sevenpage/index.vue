<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '直播平台',
            img:[
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-1.jpg',
                    content:'南台車展納智傑主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-2.jpg',
                    content:'資生堂驅黑淨白霧主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-3.jpg',
                    content:'納智傑URX5+1樂活主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-4.jpg',
                    content:'速霸陸WRX展示主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-5.jpg',
                    content:'艾杜紗櫃旁主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-6.jpg',
                    content:'資生堂心機彩妝展演'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-7.jpg',
                    content:'SODASTREAM 氣泡水機主持'
                },
                {
                    src:'/H5/4/img/sevenpage/sevenpage-img-8.jpg',
                    content:'亞太電信長期配合主持'
                },
            ]
        }
    },
    components: {
        Backgroundpage,
    },
    props:[
        'active'
    ],
    mounted() {
        var width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
        if (width < 768 ){
            this.img[0].content = '納智傑車展主持'
            this.img[1].content = '資生堂產品主持'
            this.img[2].content = '納智傑樂活主持'
            this.img[3].content = '速霸陸展示主持'
            this.img[4].content = '艾杜紗櫃旁主持'
            this.img[5].content = '資生堂彩妝展演'
            this.img[6].content = 'SODA主持'
            this.img[7].content = '亞太電信主持'
            
        }
    },

}
</script>

<style>

</style>