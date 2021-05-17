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
                    title:'公司產品',
                    page:'5'
                },
                {
                    title:'項目案例',
                    page:'6'
                },
                {
                    title:'聯繫我們',
                    page:'7'
                }
            ]
        }
    },
    props:[
        'pageMoveto',
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