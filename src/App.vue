<template>
    <div id="app">
        <TheHeader />
        <main>
            <router-view></router-view>
        </main>
        <TheFooter />
    </div>
</template>

<script>
import TheHeader from "@/components/TheHeader.vue";
import TheFooter from "@/components/TheFooter.vue";

export default {
    name: "app",
    components: {
        TheHeader,
        TheFooter
    }
};
</script>

<style>
* {
    box-sizing: border-box;
}

body,
ul,
li,
h1,
h2,
p {
    margin: 0px;
    padding: 0px;
}

ul {
    list-style: none;
}

body {
    font-family: "IBM Plex Sans";
    color: #345;
    background: url("./assets/pattern.svg") repeat top;
}

a {
    color: #345;
    list-style: none;
    text-decoration: none;
}

img {
    max-width: 100%;
    display: block;
}

.btn {
    display: block;
    padding: 30px 30px;
    background: #87f;
    border-radius: 4px;
    color: white;
    text-align: center;
    font-size: 1rem;
    box-shadow: 0 4px 8px rgb(30, 60, 90, 0.2);
    transition: all 0.3s;
    border: none;
    font-family: "IBM Plex Sans";
    cursor: pointer;
}

.btn:hover {
    background: #65d;
    transform: scale(1.1);
}

#app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}
main {
    flex: 1;
}
</style>