<template>
    <form action="">
        <div v-show="step===1">
            <label for="name">Name :</label>
            <input type="text" name="name" placeholder="Enter Your Name">
        </div>
        <div v-show="step===2">
            <label for="email">Email :</label>
            <input type="email" name="email" placeholder="Enter Your Email">
        </div>
        <div v-show="step===3">
            <label for="pwd">Password :</label>
            <input type="password" name="pwd" placeholder="Enter Your Password">
        </div>

        <button type="button" @click="backStep" v-if="step>1">BACK</button>
        <button type="button" @click="nextStep">{{ step<3?"NEXT":"SUBMIT" }}</button>
    </form>
</template>
<script>
    export default{
        data(){
            return{
                step:1,
            }
        },
        methods:{
            nextStep(){
                if(this.step<3)
                this.step++;
            },
            backStep(){
                if(this.step>1)
                this.step--;
            }
        }
    }
</script>
<style scoped>

</style>