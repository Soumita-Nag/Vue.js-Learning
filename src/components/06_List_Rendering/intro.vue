<template>
    <div class="container">
        <div class="card" v-for="(book,index) in books">
        <h2>{{book.name}}</h2>
        <h4>Book No: {{index+1}}</h4>
        <h3>Author: {{book.author}}</h3>
        <h4>Price: {{book.price}}</h4>
        <h5>publisher: {{publisher}}</h5>
        <span id="tag" v-for="(tag,ind) in book.tags">{{ tag }}{{ ind<tag.length-1?" ,":"" }}</span>
        <button>Buy</button>
    </div>
    </div>
</template>
<script>
    export default{
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
                        tags:['scifi','thriller'],
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
                publisher: "bloomsberry"
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
        display: inline;
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