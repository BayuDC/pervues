<script>
import BookCard from "./BookCard.vue";
import Floating from "./Floating.vue";
import Button from "./Button.vue";

export default {
    name: "BookList",
    props: ["books"],
    components: {
        BookCard,
        Button,
        Floating,
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
            <BookCard :book="book" />
        </div>
    </div>

    <Floating>
        <Button type="success" size="large">Add Book</Button>
    </Floating>
</template>
