<template>
  <div id="app"
  @touchstart="touchStarAudio">
      <div class="topcover" :class="{'active' : !active}"></div>
        <audio id="audio" autoplay>
            <source src="/music/GetUp by RazBurg Artlist.wav" type="audio/mpeg">
        </audio>
        <button class="btn-music" id="btn-music"
        :class="{'paused':btnPuased}"
        @click="audioAutoPlay">
              <i class="fas fa-music"></i>
        </button>
        <div class="arrow-up">
          <i class="fas fa-angle-double-up"></i>
        </div>
      <full-page :options="options" ref="fullpage"  >
        <div class="section"  >
          <Mainpage :active="active"/>
        </div>  
        <div class="section" 
        @mousemove="touchStarAudio">
          <Twopage  :pageMoveto="pageMoveto" :active="active"/>
        </div>         
        <div class="section" >
          <Threepage :pageBackIndex="pageBackIndex" :active="active" />
        </div>      
        <div class="section" >
          <Fourpage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>     
        <div class="section" >
          <Fivepage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>    
        <div class="section" >
          <Sixpage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>     
        <div class="section" >
          <Sevenpage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>     
        <div class="section" >
          <Eightpage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>    
        <div class="section" >
          <Ninepage :pageBackIndex="pageBackIndex" :active="active"/>
        </div>    
      </full-page>
  </div>
</template>

<script>
import './assets/css/app.scss'
import Mainpage from './components/mainpage/index'
import Twopage from './components/twopage/index'
import Threepage from './components/threepage/index'
import Fourpage from './components/fourpage/index'
import Fivepage from './components/fivepage/index'
import Sixpage from './components/sixpage/index'
import Sevenpage from './components/sevenpage/index'
import Eightpage from './components/eightpage/index'
import Ninepage from './components/ninepage/index'

export default {
  data(){
    return {
      mobilAudio:false,
      btnPuased:true,
      active:false,
      options: {
        licenseKey: "OPEN-SOURCE-GPLV3-LICENSE",
        //是否顯示導航，預設為false
        navigation: true,
        
        //頁面滾動速度
        scrollingSpeed: 700,
        //動畫
        controlArrows: true,
        loopBottom:true,
        loopTop:true ,
        onLeave: this.movePage,
        afterLoad: this.movePageAfter,
      },
    }
  },
  name: 'App',
  components: {
    Mainpage,
    Twopage,
    Threepage,
    Fourpage,
    Fivepage,
    Sixpage,
    Sevenpage,
    Eightpage,
    Ninepage,
  },
  watch: {
    mobilAudio: function() {
        var audio = document.getElementById('audio');
        audio.play();
        if (!audio.paused){
          this.btnPuased = false;
        }
    }
  },
  methods:{
    pageBackIndex(){
      this.$refs.fullpage.api.moveTo(2);
    },
    pageMoveto(index){
      this.$refs.fullpage.api.moveTo(index);
    },
    movePage(){
      
      this.active =! this.active
      
      console.log(this.active)
    },
    movePageAfter(){
      
      this.active =! this.active
      
      console.log(this.active)
    },
    ///audio監聽
    audioAutoPlay(){
      var audio = document.getElementById('audio');
      if (audio.paused){
        console.log(123)
        audio.play();
        this.btnPuased = false;
      }
      else {
        audio.pause();
        this.btnPuased = true;
      }
    },
    touchStarAudio(){
      this.mobilAudio = true;
    }
  }
}
</script>