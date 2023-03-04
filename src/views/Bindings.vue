<template>
    <div class="home">
        <!-- <h1 class="myClass">Hello, world!</h1> -->
        <!-- Two way binding -->
        <input type="text" v-model="user" placeholder="Enter your name..." />

        <!-- One way binding -->
        <h1 class="myClass">Hello, {{ user }}!</h1>

        <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
        <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
    data() {
        return {
            user: "Teja"
        }
    }
    // name: 'HomeView',
    // components: {
    //   HelloWorld
    // }
}
</script>

<style>
.myClass {
    color: red;
}
</style>