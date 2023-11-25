<script setup>
import { ref } from "vue";
import router from "../router";

const email = ref('john@gmail.com')
const password = ref('password')

const login = async () => {
    console.log(`Email: ${ email.value } Password: ${ password.value }`);
    router.push('/dashboard')
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="form-title">
                    <h1>Login Here</h1>
                </div>
                <form @submit.prevent="login" class="signup-form">
                    <div class="form-group">
                        <input type="email" name="email" placeholder="Enter email" v-model="email">
                    </div>
                    <div class="form-group">
                        <input type="password" name="password" placeholder="Enter password" v-model="password">
                    </div>
                    <div class="form-group">
                        <input type="submit" name="login" value="Login">
                    </div>
                    <div class="form-group">
                        <span>Dont have an account?</span><a href="">Signup</a>
                        <a href="">Forgot Password?</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<style scoped>

.container{
    background-color: rgb(100, 143, 157);
    min-height: 100vh;
}
.row{
    display: grid;
    grid-template-columns: 100%;
    justify-items: center;
}

.signup-form{
    margin-top: 5%;
}

.form-title{
    margin-top: 5%;
}

.signup-form input{
    width: 500px;
    padding: 8px 10px;
    border-radius: 5px;
}

.form-group{
    margin-bottom: 1%;
}
</style>