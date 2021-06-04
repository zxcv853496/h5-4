<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: 'FEINIEL',
            content:[
                '•生日： 12/07',
                '•身高： 168',
                '•體重： 47',
                '•三圍：　34D 25 35',
                '•髮色： 黑棕長髮',
            ]
        }
    },
    props:[
        'active'
    ],
    components: {
        Backgroundpage,
    }

}
</script>

<style>

</style>