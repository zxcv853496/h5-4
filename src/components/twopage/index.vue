<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '頂尖宗旨',
            content:[
                '致力於創新行銷領域',
                '•互聯網電商平台',
                '•創意廣告',
                '•多媒體影像製作',
                '•演藝娛樂藝人栽培課程',
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