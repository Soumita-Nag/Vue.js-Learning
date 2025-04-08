<template>
    <div class="container">
        <div class="heading">
            <span class="title">Title</span>
            <button @click="check">{{ val }}</button>
        </div>
        <div class="box" :class="view">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum quod iusto error odit omnis, natus mollitia consequatur ducimus? Vitae numquam totam dolorem corrupti! Quia assumenda veniam inventore nihil commodi doloribus esse voluptate aliquid at?
        </div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                isChecked:true,
                view: "show",
                val : "-",
            }
        },
        methods:{
            check(){
                this.isChecked=!this.isChecked;
                if(this.isChecked==false){
                    this.view=null;
                    this.val="+";
                }
                else{
                    this.view="show";
                    this.val="-";
                }
            }
        }
    }
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .container{
        height: 100vh;
        width: 100vw;
        display: flex;
        align-items: center;
        /* justify-content: center; */
        flex-direction: column;
        padding-top: 200px;
    }
    .heading{
        height: 30px;
        width: 600px;
        background-color: rgb(36, 0, 125);
        display: flex;
        gap: 500px;
        padding: 5px;
    }
    .title{
        color: rgb(255, 255, 255);
        font-size: 18px;
        font-weight: bold;
    }
    button{
        width: 100px;
        border: none;
        background-color: rgb(131, 74, 255);
        border-radius: 20px;
        font-size: 18px;
        font-weight: bold;
        color: white;
    }
    .box{
        background-color: rgb(131, 74, 255);
        width: 600px;
        display: none;
    }
    .show{
        display: block;
    }
</style>