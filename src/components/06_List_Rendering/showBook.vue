<template>
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
</template>
<script>
    export default{
        data(){
            return{
                
            }
        },
        props:{
            book:Object, 
            // its receiving an object from the parent and printing it in temolate
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