<script>
import Button from "./Button.vue";

export default {
    name: "BookCard",
    props: ["title", "author"],
    components: {
        Button,
    },
};
</script>
<template>
    <div class="card border-dark">
        <div class="card-body">
            <h5 class="card-title">{{ title }}</h5>
            <h6 class="card-subtitle mb-2">{{ author }}</h6>
            <div class="d-flex justify-content-end gap-1 pt-4">
                <Button type="primary">Update</Button>
                <Button type="danger">Delete</Button>
            </div>
        </div>
    </div>
</template>