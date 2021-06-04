<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '專業優勢'
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