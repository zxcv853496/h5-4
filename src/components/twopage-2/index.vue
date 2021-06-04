<template src="./template.html">
</template>

<script>
import Backgroundpage from '../backgroundpage/index'
export default {
    data(){
        return{
            title: '接案類型',
            content:[
                '•主持',
                '•司儀',
                '•Show Girl',
                '•Demo',
                '•PG',
                '•展場',
                '•Road Show',
                '•賽事',
                '•代言',
                '•平面',
                '•接待',
                '•CF',
                '•直播',
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