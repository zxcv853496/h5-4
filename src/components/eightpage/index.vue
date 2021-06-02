<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '聯繫方式',
            connection:[
                '電話: 04-2471-9799',
                '公司地址： 台中市南屯區精誠路504號2F',
                '信箱： yongxin@yongxin-design.com'
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