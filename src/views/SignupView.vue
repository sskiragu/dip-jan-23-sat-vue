<script setup>
import { ref } from "vue";

const name = ref('John')
const email = ref('john@gmail.com')
const password = ref('password')

const signup = async () => {
    console.log(`Username: ${ name.value } Email: ${ email.value } Password: ${ password.value }`);
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="form-title">
                    <h1>Signup Here</h1>
                </div>
                <form @submit.prevent="signup" class="signup-form">
                    <div>
                        <h1>{{ name }}</h1>
                    </div>
                    <div class="form-group">
                        <input type="text" name="name" placeholder="Enter username" v-model="name">
                    </div>
                    <div class="form-group">
                        <input type="email" name="email" placeholder="Enter email" v-model="email">
                    </div>
                    <div class="form-group">
                        <input type="password" name="password" placeholder="Enter password" v-model="password">
                    </div>
                    <div class="form-group">
                        <input type="submit" name="signup" value="Signup">
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