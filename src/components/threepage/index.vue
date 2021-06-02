<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '頂尖傳媒'
        }
    },
    props:[
        'active',
    ],
    components: {
        Backgroundpage,
    }

}
</script>

<style>

</style>