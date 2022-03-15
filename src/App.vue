<script>
import Navbar from './components/Navbar.vue';
import BookList from './components/BookList.vue';

export default {
    name: 'App',
    components: {
        Navbar,
        BookList,
    },
    data() {
        return {
            books: [
                { id: 1, title: 'Buku Keren', author: 'Saya Sendiri' },
                { id: 2, title: 'Buku Keren Lagi', author: 'Saya Sendiri' },
                { id: 3, title: 'Buku Rusak', author: 'Temen Saya' },
                { id: 4, title: 'Ga Ada Judulnya', author: 'Ga Tau Siapa' },
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
