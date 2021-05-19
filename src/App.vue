<template>
  <div id="app">
      <full-page :options="options" ref="fullpage" >
        <div class="section" >
          <Mainpage/>
        </div>  
        <div class="section" >
          <Twopage :pageMoveto="pageMoveto"/>
        </div>         
        <div class="section" >
          <Threepage :pageBackIndex="pageBackIndex"/>
        </div>      
        <div class="section" >
          <Fourpage :pageBackIndex="pageBackIndex"/>
        </div>     
        <div class="section" >
          <Fivepage :pageBackIndex="pageBackIndex"/>
        </div>    
        <div class="section" >
          <Sixpage :pageBackIndex="pageBackIndex"/>
        </div>     
        <div class="section" >
          <Sevenpage :pageBackIndex="pageBackIndex"/>
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

export default {
  data(){
    return {
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
    Sevenpage
  },
  methods:{
    pageBackIndex(){
      this.$refs.fullpage.api.moveTo(2);
    },
    pageMoveto(index){
      this.$refs.fullpage.api.moveTo(index);
    },
  }
}
</script>