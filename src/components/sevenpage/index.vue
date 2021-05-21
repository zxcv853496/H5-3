<template src='./template.html'>
  
</template>

<script>
export default {

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