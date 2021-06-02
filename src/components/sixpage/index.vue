<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '資歷',
            data:[
                {
                    img:'/img/sixpage/sixpage-img-1.jpg',
                },
                {
                    img:'/img/sixpage/sixpage-img-2.jpg',
                },
                {
                    img:'/img/sixpage/sixpage-img-3.jpg',
                },
            ],
            content:[
                '2017   LOreal Color Trophy 髮型秀攝影造型',
                '2017   實踐大學服裝設計系 畢業展 後台造型',
                '2016    獵人工作室 演員形象造型',
                '2016    1922 網路商城攝影造型 / 美編',
                '2015    國際美容美髮競賽亞洲盃創意面具組 優選',
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