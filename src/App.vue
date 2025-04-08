<script>
import count from '@/components/02_Examples/count.vue'

// import Hello from '@/components/02_Examples/Hello.vue'

// import Header from '@/components/01_demo_page/Header.vue'
// import Body from '@/components/01_demo_page/Body.vue'
// import Footer from '@/components/01_demo_page/Footer.vue'

// import Counter from '@/components/03_Counter/Counter.vue'

// import Directives from '@/components/02_Examples/directives.vue'

import toggleText from '@/components/02_Examples/toggleText.vue' 

export default{
  components:{
    // Hello,
    // count,
    // Header,
    // Body,
    // Footer,
    // Counter,
    // Directives,
    toggleText,
  },
  data(){
    return{
      isActive:true,
    }
  }
}
</script>

<template>
  <!-- Components for 01_demo_page starts -->
  <!-- <Header/>
  <Body/>
  <Footer/> -->
  <!-- Components for 01_demo_page ends -->

<!-- Components for 02_Examples starts -->
  <!-- <h1>Hello from Soumita</h1>
  <Hello/> -->
  <!-- <count/> -->
<!-- Components for 02_Examples ends -->

<!-- <Counter/> -->

 <!-- <Directives/> -->

  <toggleText :class="{'test':isActive}"/>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
::-webkit-scrollbar{
  background-color: black;
  width: 1px;
}
::-webkit-scrollbar-thumb{
  background-color: rgb(0, 0, 0);
}
.test{
  background-color: red;
}
</style>
