<script>
    export default{
        data(){
            return{
                count:0,
                normal: "default",
                bold : "boldText",
                isOk:false,
            }
        },
        methods:{
            check(){
                if(this.count>5){
                    // this.normal="danger"
                    this.isOk=true;
                }
            },
        }
    }
</script>

<template>
    <div class="container">
        <!-- Style changing using binding to arrays -->
        <!-- <h1 :class="[normal,bold]">This text's style is gonna toggle</h1> -->
        
        <!-- this can also be written as -->
        <h1 :class="[isOk ? 'danger' : 'default' , bold]">This text's style is gonna toggle</h1>

        <button @click="count++,check()">Count is : {{ count }}</button>
    </div>
</template>
<style scoped>
.container{
    height: 100vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
    button{
        font-weight: bold;
        height: 40px;
        width: 120px;
        font-size: 16px;
        cursor: pointer;
    }
    .default{
        color: green;
    }
    .boldText{
        font-weight: bold;
    }
    .danger{
        background-color: red;
    }
</style>