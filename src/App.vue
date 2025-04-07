<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
// import count from '@/components/count.vue'
// import Hello from '@/components/Hello.vue'

import Header from '@/components/Header.vue'
import Body from '@/components/Body.vue'
import Footer from '@/components/Footer.vue'

export default{
  components:{
    // Hello,
    // count,
    Header,
    Body,
    Footer,
  }
}
</script>

<template>
  <!-- <h1>Hello from Soumita</h1>
  <count/> -->

  <!-- <Hello/> -->

  <Header/>
  <Body/>
  <Footer/>
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
</style>
