<template>
    <div>
        <h1>The User Page</h1>
        <hr>
        <!-- <p>Loaded ID: {{id}}</p> -->
        <button @click="navigateToHome">Go to Home</button>
        <hr>
        <transition name="slide" mode="out-in">
            <router-view></router-view>
        </transition>
    </div>
</template>

<script>
export default {
    methods: {
        navigateToHome() {
            this.$router.push({name: 'home'});
        }
    }
}
</script>

<style>
.slide-enter {
    opacity: 0;
}
.slide-enter-active {
    transition: opacity .5s ease;
}
.slide-leave-active {
    opacity: 0;
    transition: opacity .5s ease;
}
</style>
