<template src='./template.html'>
  
</template>

<script>
import Slick from "vue-slick"
export default {
    components: { Slick },
    data() {
        return {
            data:[
                {
                    title:'公司地址：',
                    content:'台中市南屯區精誠路504號2F'
                },
                {
                    title:'聯繫電話：',
                    content:'04-2471-9799'
                },
                {
                    title:'信箱：',
                    content:'yongxin@yongxin-design.com'
                },
                {
                    title:'官網連結',
                    content:'https://www.yongxin-design.com/'
                },
            ]
        };
    },
    props: [
        'active',
        'pageBackIndex'
    ],
    methods:{
        pageMove(){
            this.pageBackIndex()
        }
    }
}
</script>

<style>

</style>