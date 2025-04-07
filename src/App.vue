<script>
// import count from '@/components/02_Examples/count.vue'
// import Hello from '@/components/02_Examples/Hello.vue'

import Header from '@/components/01_demo_page/Header.vue'
import Body from '@/components/01_demo_page/Body.vue'
import Footer from '@/components/01_demo_page/Footer.vue'

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
  <!-- Components for 01_demo_page starts -->
  <Header/>
  <Body/>
  <Footer/>
  <!-- Components for 01_demo_page ends -->

<!-- Components for 02_Examples starts -->
  <!-- <h1>Hello from Soumita</h1>
  <count/> -->
  <!-- <Hello/> -->
<!-- Components for 02_Examples ends -->

</template>

<style>
/* Style for 01_demo_page starts */
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

/* Style for 01_demo_page ends */
</style>
