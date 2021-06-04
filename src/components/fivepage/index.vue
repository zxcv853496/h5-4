<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '宣傳照',
            data:[
                {
                    img:'/H5/4/img/fivepage/1.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/2.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/3.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/4.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/5.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/6.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/7.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/8.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/9.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/10.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/11.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/12.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/13.jpg'
                },
                {
                    img:'/H5/4/img/fivepage/14.jpg'
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