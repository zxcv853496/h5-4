<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '直播主',
            data:[
                {
                    img:'/img/fivepage/1.jpg'
                },
                {
                    img:'/img/fivepage/2.jpg'
                },
                {
                    img:'/img/fivepage/3.jpg'
                },
                {
                    img:'/img/fivepage/4.jpg'
                },
                {
                    img:'/img/fivepage/5.jpg'
                },
                {
                    img:'/img/fivepage/6.jpg'
                },
                {
                    img:'/img/fivepage/7.jpg'
                },
                {
                    img:'/img/fivepage/8.jpg'
                },
                {
                    img:'/img/fivepage/9.jpg'
                },
                {
                    img:'/img/fivepage/10.jpg'
                },
                {
                    img:'/img/fivepage/11.jpg'
                },
                {
                    img:'/img/fivepage/12.jpg'
                },
                {
                    img:'/img/fivepage/13.jpg'
                },
                {
                    img:'/img/fivepage/14.jpg'
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
    methods: {
        DelayFormat(index){
            if(this.active){
                index = index*1
                return `animate__animated animate__zoomIn animate__delay__decimals-${index}s`
            }
        }
    }

}
</script>

<style>

</style>