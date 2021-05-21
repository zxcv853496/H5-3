<template src="./template.html">
  
</template>

<script>
export default {
    data(){
        return{
            items:[
                {
                    title:'公司簡介',
                    page:'3'
                },
                {
                    title:'企業目標',
                    page:'4'
                },
                {
                    title:'公司產品-名片',
                    page:'5'
                },
                {
                    title:'公司產品-網頁',
                    page:'6'
                },
                {
                    title:'公司產品-網頁',
                    page:'7'
                },
                
                {
                    title:'方案選購',
                    page:'8'
                },
                {
                    title:'聯繫我們',
                    page:'9'
                }
            ]
        }
    },
    props:[
        'pageMoveto',
        'active',
    ],
    methods:{
        thispageMoveto(index){
            this.pageMoveto(index)
        }
    }
}
</script>

<style>

</style>