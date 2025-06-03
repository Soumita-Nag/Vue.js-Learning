<template>
    <div class="container">
        <!-- without component rendering -->
        <div class="card" v-for="(book,index) in books" :key="index">
            <h2>{{book.name}}</h2>
            <h4>Book No: {{index+1}}</h4>
            <h3>Author: {{book.author}}</h3>
            <h4>Price: {{book.price}}</h4>
            <h5>publisher: {{publisher}}</h5>
            <span id="tag" v-if="book.tags.length!==0">
                <!-- this section will be visible if and only if tags are given in the books -->
                <b>Tags:&nbsp;</b>
                <p v-for="(tag,ind) in book.tags">
                    {{ tag }}{{ ind<book.tags.length-1?",&nbsp;":"" }}
                    <!-- printing each tag with a , except for the last tag where , is not needed -->
                </p>
            </span>
            <button>Buy</button>
        </div>

        <!-- with component rendering -->
        <div v-for="mybook in books">
            <div class="card" >
                <showBook :book="mybook"/>
                <!-- sending the object to the child component -->
            </div>
        </div>
    </div>
    <div class="box">
        <div class="box1">
            <ul>
                <li v-for="(value,key,index) in myObject"><b>{{ index+1 }}. {{ key }}:</b> {{ value }}</li>
                <!-- iterating object using v-for, value and key both are accessible, also index can also be accessible-->
                 <!-- syntax: (value,key,index) -->
            </ul>
            <span v-for="n in 10">{{ n }}&nbsp;</span><br>
            <span v-for="n in books.length">{{ n }}&nbsp;</span>
            <!-- it will start counting from 1 instead of zero -->
        </div>
        <div class="box2">
            <!-- <div v-for="todo in todos" v-if="todo.isComplete"> -->
                <!-- Wrong appreach: if we use vif and vfor in same element, it may show error -->
                <!-- precedence of vif is higher than vfor, here we're tring to access todo before definging it -->
                <!-- we have to do it in two steps -->
            <div v-for="todo in todos">
                <span v-if="todo.isComplete">{{ todo.name }}</span>
            </div>
        </div>
        <div class="box3">
            <!-- printing a component multiple time using vfor -->
            <span v-for="n in 3">
                <hello/>
            </span>
        </div>
    </div> 
</template>
<script>
import hello from './hello.vue';
import showBook from './showBook.vue';
    export default{
        components:{
            hello,
            showBook,
        },
        data(){
            return{
                books:[
                    {
                        name:"Sherlock Holmes",
                        price: 350,
                        author:"Arthur Conan Doyle",
                        tags:['scifi','mystery','crime','thriller'],
                    },
                    {
                        name:"HP and the Cursed Child",
                        price: 480,
                        author:"J.K.Rowling",
                        // tags:['scifi','thriller'],
                        tags:[],
                    },
                    {
                        name:"Sonar Kella",
                        price: 270,
                        author:"Satyajit Roy",
                        tags:['mystery','crime','thriller'],
                    },
                    {
                        name:"Half Girlfriend",
                        price: 250,
                        author:"Chetan Bhagat",
                        tags:['romantic'],
                    },
                ],
                publisher: "bloomsberry",
                myObject: {
                    title: 'How to do lists in Vue',
                    author: 'Jane Doe',
                    publishedAt: '2016-04-10'
                },
                todos:[
                    {
                        name:"dbms",
                        isComplete:false
                    },
                    {
                        name:"os",
                        isComplete:true
                    },
                    {
                        name:"java",
                        isComplete:true
                    },
                    {
                        name:"coa",
                        isComplete:false
                    },
                    {
                        name:"dsa",
                        isComplete:false
                    },
                ]      
            }
        },
        methodes:{
            
        },
    }
</script>
<style scoped>
    .card{
        height: 300px;
        width: 300px;
        border: 2px solid black;
        background-color: blueviolet;
        border-radius: 20px;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 10px;
    }
    #tag{
        display: flex;
    }
    .container{
        height: 100vh;
        width: 100vw;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 100px 0;
        gap: 50px;
        
    }
    .box{
        height: 100vh;
        width: 100vw;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 100px 0;
        gap: 50px;
        
    }
    button{
        cursor: pointer;
        height: 30px;
        width: 70px;
        border: 3px solid rgb(211, 174, 247);
        border-radius: 20px;
        background-color: rgb(74, 2, 142);
        color: white;
        font-weight: bold;
    }
</style>   