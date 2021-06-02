<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '公益關懷'
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