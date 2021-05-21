<template src='./template.html'>
  
</template>

<script>
export default {
    data() {
        return {
            options:[
                    "方案選購",
                    "品牌設計",
                    "行銷規劃",
                    "網站設計",
                    "多媒體設計",
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