<script>
import Navbar from "./components/Navbar.vue";
import BookList from "./components/BookList.vue";

export default {
    name: "App",
    components: {
        Navbar,
        BookList,
    },
    data() {
        let now = Date.now();

        return {
            books: [
                { id: now++, title: "Buku Keren", author: "Saya Sendiri" },
                { id: now++, title: "Buku Keren Lagi", author: "Saya Sendiri" },
                { id: now++, title: "Buku Rusak", author: "Temen Saya" },
                { id: now++, title: "Ga Ada Judulnya", author: "Ga Tau Siapa" },
            ],
        };
    },
};
</script>

<template>
    <div class="mb-4">
        <Navbar />
    </div>
    <div class="container">
        <BookList :books="books" />
    </div>
</template>
