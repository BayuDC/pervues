<script>
import Navbar from "./components/Navbar.vue";

export default {
    name: "App",
    components: {
        Navbar,
    },
};
</script>

<template>
    <div class="mb-4">
        <Navbar />
    </div>
    <div class="container">
        <h1>Hello World</h1>
    </div>
</template>
