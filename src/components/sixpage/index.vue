<template src='./template.html'>
  
</template>

<script>
import Slick from "vue-slick"
export default {
    components: { Slick },
    data() {
        return {


        };
    },
    props: [
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