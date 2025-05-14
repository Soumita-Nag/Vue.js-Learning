<template>
    <form action="">
        <div>
            <label for="name">Name :</label>
            <input type="text" name="name" placeholder="Enter Your Name">
            <p v-if="err.name">{{ err.name }}</p>
        </div>
        <div>
            <label for="email">Email :</label>
            <input type="email" name="email" placeholder="Enter Your Email">
            <p v-if="err.email">{{ err.email }}</p>
        </div>
        <div>
            <label for="pwd">Password :</label>
            <input type="password" name="pwd" placeholder="Enter Your Password">
            <p v-if="err.pwd">{{ err.pwd }}</p>
        </div>

        <!-- <p v-if="err">{{ err }}</p> -->

        <button type="button" @click="validate">Submit</button>
    </form>
</template>
<script>
    export default{
        data(){
            return{
                err:{
                    name:null,
                    email:null,
                    pwd:null,
                },
            }
        },
        methods:{
            validate(){
                // if(!this.err){
                //     this.err="Invalid Credentials";
                // }
                // else{
                //     this.err=null;
                // }

                this.err.name='Invalid Name'
                this.err.email='Invalid Email'
                this.err.pwd='Invalid Password'
            }
        }
    }
</script>
<style scoped>

</style>