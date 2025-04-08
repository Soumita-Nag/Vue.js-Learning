<template>
    <h1>Books</h1>
    <h3>{{ isEven() }}</h3>
    <h3>{{ isEven() }}</h3>
    <h3>{{ isEven() }}</h3>
    <!-- here isEven function gets called 3 times though the result will not gonna change before the 2nd call -->
    <!-- to reduce function call, we use computed section -->
    <!-- in computed, there is a function which returns the result and stores the result until the dependecies are changed. hence here computedIsEven gets called only one time as the no of books did not changes before calling the function again -->
    <h3>{{ computedIsEven }}</h3>
    <h3>{{ computedIsEven }}</h3>
    <h3>{{ computedIsEven }}</h3>
</template>

<script>
    export default{
        data(){
            return{
                books:[
                    {id: 1, name: "Harry Potter"},
                    {id: 2, name: "Harry Potter"},
                    {id: 3, name: "Harry Potter"},
                ]
            }
        },
        computed:{
            computedIsEven(){
                console.log("Computed is called")
                return this.books.length % 2=== 0? "EVEN" : "ODD"
            }
        },
        methods:{
            isEven(){
                console.log("isEven is called")
                return this.books.length % 2=== 0? "EVEN" : "ODD"
            }
        }
    }
</script>

<style>

</style>