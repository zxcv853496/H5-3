<template src='./template.html'>
  
</template>

<script>
import Slick from "vue-slick";

export default {
  components: { Slick },
  data() {
    return {
      slickOptions: {
        slidesToShow: 2,
        slidesToScroll: 2,
        autoplay: true,
        autoplaySpeed: 1000,
      },
        list:[
            {
                img:'/img/fivepage/card1.jpg'
            },
            {
                img:'/img/fivepage/card2.jpg'
            },
            {
                img:'/img/fivepage/card3.jpg'
            },
            {
                img:'/img/fivepage/card4.jpg'
            },
            {
                img:'/img/fivepage/card5.jpg'
            },
            {
                img:'/img/fivepage/card6.jpg'
            },
        ]
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
};
</script>

<style>

</style>

