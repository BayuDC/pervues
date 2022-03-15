<script>
import BookCard from './BookCard.vue';
import Button from './Button.vue';

export default {
    name: 'BookInfo',
    props: ['book'],
    components: {
        BookCard,
        Button,
    },
};
</script>

<template>
    <BookCard>
        <template #default>
            <h5 class="card-title">{{ book.title }}</h5>
            <h6 class="card-subtitle mb-2">{{ book.author }}</h6>
        </template>
        <template #btn-group>
            <Button type="primary" size="small">Update</Button>
            <Button type="danger" size="small"> Delete </Button>
        </template>
    </BookCard>
</template>
