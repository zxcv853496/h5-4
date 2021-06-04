<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '聯繫方式',
            connection:[
                '電話: 0956352672',
                '信箱： VOLVO914074@GMAIL.COM'
            ]
        }
    },
    props:[
        'active'
    ],
    components: {
        Backgroundpage,
    },

}
</script>

<style>

</style>