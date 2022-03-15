<script>
import BookInfo from "./BookInfo.vue";
import BookForm from "./BookForm.vue";
import Button from "./Button.vue";

export default {
    name: "BookList",
    props: ["books"],
    components: {
        BookInfo,
        BookForm,
        Button,
    },
    created() {
        this.books = this.$props.books;
    },
    data() {
        return { books: [] };
    },
    methods: {
        addBook({ title, author }) {
            this.books.push({ id: Date.now(), title, author });
        },
        editBook({ id, title, author }) {
            const book = this.books.find((book) => book.id == id);

            book.title = title;
            book.author = author;
            book.editMode = undefined;
        },
        deleteBook(id) {
            this.books = this.books.filter((book) => book.id != id);
        },
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
            <BookForm v-if="book.editMode" :book="book" @save="editBook" />
            <BookInfo v-else :book="book" @destroy="deleteBook" />
        </div>
        <div class="col-md-3 col-sm-4 col-12">
            <BookForm @save="addBook" />
        </div>
    </div>
</template>
