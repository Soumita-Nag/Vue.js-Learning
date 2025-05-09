<template>
    <h1 v-if="cnt==0">Hello Guys</h1>
    <h1 v-else-if="cnt==1">Good Morning</h1>
    <h1 v-else>Bye Guys</h1>
    <button @click="toggle">toggle</button>
</template>
<script>
    export default{
        data(){
            return{
                // isActive:true,
                cnt : 0,
            }
        },
        methods:{
            toggle(){
                this.cnt++;
                if(this.cnt>2)
                this.cnt=0;
            }
        }
    }
</script>
<style scoped>

</style>