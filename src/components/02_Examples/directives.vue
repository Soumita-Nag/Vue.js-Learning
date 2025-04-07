<template>
    <!-- v-html -->
    
    {{ message }} 
    <!-- html tags does not works inside {{  }}, it reads the text as plain text -->
    <!-- To resolve this, we use v-html, v-html executes html tags written within the string -->
    <div v-html="message"></div>

</template>

<script>
    export default{
        data(){
            return{
                message : "<h1>Hello Soumita</h1>",
            }
        }
    }
</script>

<style>

</style>