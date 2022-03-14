<script>
export default {
    name: "BookInfo",
    props: ["title", "author"],
};
</script>

<template>
    <h5 class="card-title">{{ title }}</h5>
    <h6 class="card-subtitle mb-2">{{ author }}</h6>
</template>