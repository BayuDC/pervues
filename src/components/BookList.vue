<script>
import BookCard from "./BookCard.vue";
import Button from "./Button.vue";

export default {
    name: "BookList",
    props: ["books"],
    components: {
        BookCard,
        Button,
    },
};
</script>

<template>
    <div class="row">
        <div
            v-for="book in books"
            :key="book.id"
            class="col-md-3 col-sm-4 col-12"
        >
            <BookCard :title="book.title" :author="book.author" />
        </div>
    </div>
</template>
