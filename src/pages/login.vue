<script setup>
import {ref} from "vue";
import { useRouter } from "vue-router";
import useAuth from "../composable/useAuth";

const { isAuthenticated, login } = useAuth();

const username = ref("");
const password = ref("");

const router = useRouter();

const logginIn = () => {
    if (isAuthenticated.value) {
        router.push("/");
    }
};
</script>

<template>
<div class="flex flex-col items-center space-y-12 justfiy-center min-h-screen-nonav">
    Logged in: {{ isAuthenticated }}
    <div class="flex items-center justify-center overflow-hidden bg-gray-200 rounded-lg shadow-2xl">         
        <img class="h-64" src="../assets/bglogin.png" alt="Hello BG"/>
        <form @submit.prevent="login(username, password)" class="flex flex-col p-4 space-y-4">
            <input type="text" class="p-2 border-2 rounded-lg" placeholder="Username" v-model="username"/>
            <input type="password" class="p-2 border-2 rounded-lg" placeholder="Password" v-model="password"/>
            <button type="submit" @submit.prevent="login(username, password)" class="py-2 text-indigo-200 bg-indigo-600 rounded-lg">Login</button>
        </form>
    </div>
</div>
</template>