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
                    src:'/img/sevenpage/1.jpg',
                    content:'twitch'
                },
                {
                    src:'/img/sevenpage/2.jpg',
                    content:'youtube'
                },
                {
                    src:'/img/sevenpage/3.jpg',
                    content:'17'
                },
                {
                    src:'/img/sevenpage/4.jpg',
                    content:'king kong'
                },
            ]
        }
    },
    components: {
        Backgroundpage,
    },
    props:[
        'active'
    ]

}
</script>

<style>

</style>