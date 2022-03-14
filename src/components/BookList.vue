<script>
export default {
    name: "BookList",
    props: ["books"],
};
</script>

<template>
    <ul>
        <li v-for="book in books" :key="book.id">{{ book.title }}</li>
    </ul>
</template>