<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '粉絲專業',
            img: '/H5/4/img/fourpage/fourpage-img-mobile.jpg'
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
        if (width >= 768 ){
            this.img = '/H5/4/img/fourpage/fourpage-img.jpg'
        }
    },
    methods: {

    }

}
</script>

<style>

</style>