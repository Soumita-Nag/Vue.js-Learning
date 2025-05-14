<template>
    <h1 v-if="isLoading">Loading...</h1>
    <h1 v-else-if="userdata">{{userdata}}</h1>
    <h1 v-else-if="err">{{err}}</h1>
</template>
<script>
    export default{
        data(){
            return{
                isLoading:true,
                userdata:null,
                err:null,
            }
        },
        methods:{
            fetchData(){
                setTimeout(() => {
                    // this.userdata=['soumita','aku','anu'];
                    this.err="Unable to Fetch Data!!!"
                    this.isLoading=false;
                }, 3000);
            }
        },
        mounted(){
            this.fetchData();
        }
    }
</script>
<style>

</style>