<script>
import BookCard from "./BookCard.vue";
import Button from "./Button.vue";
import Input from "./Input.vue";

export default {
    name: "BookForm",
    components: { Input, Button, BookCard },
    props: ["text"],
    methods: {
        onSubmit() {
            console.log(this.title);
            console.log(this.author);
        },
    },
    data() {
        return {
            title: "",
            author: "",
        };
    },
};
</script>

<template>
    <form @submit.prevent="onSubmit">
        <BookCard>
            <template #default>
                <h5 class="card-title">{{ text }}</h5>

                <Input v-model="title" label="Title" name="title" />
                <Input v-model="author" label="Author" name="author" />
            </template>
            <template #btn-group>
                <Button type="success" size="small">Save</Button>
            </template>
        </BookCard>
    </form>
</template>
