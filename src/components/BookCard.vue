<script>
export default {
    name: "BookCard",
    props: ["title", "author"],
};
</script>
<template>
    <div class="card border-dark">
        <div class="card-body">
            <h5 class="card-title">{{ title }}</h5>
            <h6 class="card-subtitle mb-2">{{ author }}</h6>
        </div>
    </div>
</template>