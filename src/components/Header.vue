<template>
    <div class="container">
        <h1>Soumita</h1>
        <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Profile</a></li>
        <li><a href="#">Memories</a></li>
        <li><a href="#">Education</a></li>
        </ul>
    </div>
</template>
<style scoped>
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
    .container{
        height: 100px;
        width: 100vw;
        background-color: indigo;
        /* margin:0vw 0.1vw; */
        display: flex;
        color: white;
        justify-content: center;
        align-items: center;
        position: sticky;
        top: 0;
    }
    ul{
        display: flex;
        gap: 20px;
        padding-left: 65vw ;
        align-items: center;
        font-size: 18px;
    }
    li{
        list-style: none;
    }
    a{
        text-decoration: none;
        color: white;
    }
    a:hover{
        text-decoration: underline;
        color: rgb(255, 205, 130);
        font-size: 20px;
    }
</style>