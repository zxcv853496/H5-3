<template src='./template.html'>
  
</template>

<script>
import Slick from "vue-slick";

export default {
  components: { Slick },
  data() {
    return {
        mobil_active:false,
        slickOptions: {
            slidesToShow: 1,
            slidesToScroll: 1,
            autoplay: true,
            autoplaySpeed: 1000,
            arrows:false,
            pauseOnDotsHover:true,
        },
        list:[
            {
                img:'/H5/3/img/fivepage/card1.jpg'
            },
            {
                img:'/H5/3/img/fivepage/card2.jpg'
            },
            {
                img:'/H5/3/img/fivepage/card3.jpg'
            },
            {
                img:'/H5/3/img/fivepage/card4.jpg'
            },
            {
                img:'/H5/3/img/fivepage/card5.jpg'
            },
            {
                img:'/H5/3/img/fivepage/card6.jpg'
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
        },
        handleTouchstart(){
            this.mobil_active =! this.mobil_active
        },
        handleTouchend(){
            this.mobil_active =! this.mobil_active
        },
    }
};
</script>

<style>

</style>

