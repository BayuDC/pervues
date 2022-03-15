<script setup>
import BookInfo from './BookInfo.vue';
import BookForm from './BookForm.vue';
import Floating from './Floating.vue';
import Button from './Button.vue';
</script>
<script>
export default {
    name: 'BookList',
    props: ['books'],
    components: {
        BookInfo,
        BookForm,
        Button,
        Floating,
    },
    methods: {
        destroy(id) {
            this.books = this.books.filter(book => book.id != id);
        },
    },
    data() {
        return {
            books: [],
        };
    },
    created() {
        this.books = this.$props.books;
    },
};
</script>

<template>
    <div class="row">
        <div v-for="book in books" :key="book.id" class="col-md-3 col-sm-4 col-12">
            <BookInfo :book="book" />
        </div>
        <div class="col-md-3 col-sm-4 col-12">
            <BookForm />
        </div>
    </div>

    <Floating>
        <Button type="success" size="large">Add Book</Button>
    </Floating>
</template>
