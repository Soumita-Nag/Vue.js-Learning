<template>
    <!-- binds the whole object of attributes inside a tag -->
    <h1 v-bind="objAtts">Counter</h1>

    <!-- class and style binding , normal class can also be used with v-bind. if isActive is true success class will apply otherwise not.-->
    <!-- <h2 class="normal" :class="{'success':isActive, 'danger':hasError}">The counter is given bellow</h2> -->

     <!-- this line can also be written as:  -->
    <h2 :class="objClass">The counter is given bellow</h2>

    <div class="container">
        <button @click="Decrement" id="dec" :disabled="dec">DECREASE</button>
        <!-- v-bind:class or :class helps to bind class or any other attribute with a dynamic value. use : before the attribute -->
         <!-- if we assign null for the value, then the class will be dynamically removed -->
        <h1 :class="color">{{ count }}</h1> 
        <!-- count state can be accessible inside template using {{  }} which is called mustaches -->
        <button @click="Increment" id="inc" :disabled="inc">INCREASE</button>
        <!-- we can use v-on in place of @ in @click == v-on:click -->
        
    </div>
    <h2 :class="color">{{ (count>=0)?(count>5)?"Success":"Normal":"Danger" }}</h2> 
    <h2 :class="color">{{ count%2==0 ? "Even" : "Odd" }}</h2> 
    <h2 :class="color">{{ prime() }}</h2> 
    <!-- +,-, ternary operators can be used inside {{  }} -->
</template>

<script>
export default{
    data(){
        return{
            count : 0, //Called state, like a key-value paire, count stores 0
            color : 'normal',
            inc : false,
            dec : false,
            objAtts:{
                id: 'underline',
                class : 'pink',
            },
            // isActive:false,
            // hasError: false,
            objClass:{
                normal:true,
                success:false,
                danger:false,
            },
        }
    },
    methods:{
        Increment(){
            this.count++;

            if(this.count>5){
                this.color='success';
            }
            else if(this.count>=0){
                this.color='normal';
                // this.isActive=true;
                this.objClass["success"]=true;
                // this.hasError=false;
                this.objClass["danger"]=false;
                
            }
            
            if(this.count>10)
            this.inc=true;
        else if(this.count>=-5)
        this.dec=false;
},
        Decrement(){
            this.count--;
            
            if(this.count<0){
                this.color='danger';
                // this.isActive=false;
                this.objClass["success"]=false;
                // this.hasError=true;
                this.objClass["danger"]=true;
            }
            else if(this.count<=5)
            this.color='normal';

            if(this.count<-5)
            this.dec=true;
            else if(this.count<=10)
            this.inc=false;
        },
        prime(){
            if(this.count==2)
            return "Prime";
            if(this.count==0  || this.count==1)
            return "Non Prime"
            for(let i=2;i<this.count;i++){
                if(this.count % i==0)
                return "Non Prime";
            }
            return "Prime";
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
        cursor: pointer;
    }
    #inc{
        background-color: rgb(47, 255, 141);
    }
    #dec{
        background-color: red;
    }
    .normal{
        color: blue;
    }
    .danger{
        color: red;
    }
    .success{
        color: green;
    }
    #underline{
        text-decoration: underline;
    }
    .pink{
        color: rgb(255, 0, 123);
    }
</style>