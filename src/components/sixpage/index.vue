<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '活動資歷',
            data:[
                {
                    img:'/H5/4/img/sixpage/sixpage-img-1.jpg',
                },
                {
                    img:'/H5/4/img/sixpage/sixpage-img-2.jpg',
                },
                {
                    img:'/H5/4/img/sixpage/sixpage-img-3.jpg',
                },
            ],
            content:[
                '2021   資生堂水玉光AI小白金 巨城全台首賣會主持',
                '2021   DYSON展演主持2場',
                '2021   VIVO X50活動主持',
                '2021   電玩展奧瑞吉末日餘暉SG',
                '2021   台南新光三越納智傑URX新車活動',
                '2020   南台車展納智傑URX新車活動主持',
            ]
        }
    },
    components: {
        Backgroundpage,
    },
    props:[
        'active'
    ],

}
</script>

<style>

</style>