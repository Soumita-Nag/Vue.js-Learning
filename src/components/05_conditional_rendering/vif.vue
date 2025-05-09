<template>
    <h1 v-if="cnt==0">Hello Guys</h1>
    <h1 v-else-if="cnt==1">Good Morning</h1>
    <h1 v-else>Bye Guys</h1>
    <button @click="toggle">toggle</button>

    <h1 v-show="isActive">Hey there!! </h1>
    <!-- v-show only hides the element, ie display none. but does not remove the element from the DOM. Whereas v-if removes the element from the dom completely. v-if comes with v-else-if ans v-else tag where v-show doesnt have those  -->
</template>
<script>
    export default{
        data(){
            return{
                isActive:true,
                cnt : 0,
            }
        },
        methods:{
            toggle(){
                this.cnt++;
                if(this.cnt>2)
                this.cnt=0;
                this.isActive=!this.isActive;
            }
        }
    }
</script>
<style scoped>

</style>