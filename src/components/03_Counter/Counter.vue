<template>
    <h1>Counter</h1>
    <div class="container">
        <button @click="Decrement" id="dec">DECREASE</button>
        <h1>{{ count }}</h1> 
        <!-- count state can be accessible inside template using {{  }} which is called mustaches -->
        <button @click="Increment" id="inc">INCREASE</button>
        
    </div>
</template>

<script>
export default{
    data(){
        return{
            count : 0, //Called state, like a key-value paire, count stores 0
        }
    },
    methods:{
        Increment(){
            this.count++;
        },
        Decrement(){
            this.count--;
        }
    }
}
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        display: flex;
        justify-content: center;
    }
    h1{
        margin: 50px 0px;
        font-size: 60px;
    }
    .container{
        gap: 50px;
        display: flex;
        align-items: center;
    }
    button{
        height: 40px;
        width: 120px;
        padding-top: 10px;
        border: none;
        border-radius: 20px;
        font-size: 18px;
        font-weight: bold;
    }
    #inc{
        background-color: rgb(47, 255, 141);
    }
    #dec{
        background-color: red;
    }
</style>