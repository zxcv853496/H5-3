<template src="./template.html">
  
</template>

<script>
export default {
    data(){
        return{
            mid_active: false,
            timer:0,
        }
    },
    props:[
        'active',
    ],
    created (){
        this.timer = setInterval(this.midimgMover, 4000)
    },
    mounted() {
        this.midimgMover()
    },
    methods:{
        midimgMover(){
            this.mid_active =! this.mid_active
        },

    }
    

}
</script>

<style>

</style>