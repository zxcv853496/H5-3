<template src='./template.html'>
  
</template>

<script>

export default {
    data() {
        return {


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