<template>
    <div id="app">
        <!-- Nav Bar -->
        <div class="ui fixed menu">
            <div class="ui container">
                <a href="#" class="header item">
                    <img class="logo" src="./assets/logo.png" />
                </a>
                <a class="item" :href="contactlink">Contact</a>
            </div>
        </div>

        <router-view />
    </div>
</template>

<script>
export default {
    name: "App",
    data: () => {
        return {
            contactlink: "/contact"
        };
    }
};
</script>

<style>
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 2em;
    margin-top: 4em;
}
body {
    background-color: #ffffff;
}

</style>
