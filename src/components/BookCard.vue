<script>
import Button from './Button.vue';
import BookInfo from './BookInfo.vue';
import BookForm from './BookForm.vue';

export default {
    name: 'BookCard',
    props: ['book'],
    components: {
        Button,
        BookInfo,
        BookForm,
    },
    methods: {
        destroy() {
            this.$emit('destroy', this.book.id);
        },
    },
};
</script>
<template>
    <div class="card border-dark mb-sm-4 mb-3">
        <div class="card-body">
            <BookInfo v-if="book" :title="book.title" :author="book.author" />
            <BookForm v-else />
            <div v-if="book" class="d-flex justify-content-end gap-1 pt-4">
                <Button type="primary" size="small">Update</Button>
                <Button @click="destroy" type="danger" size="small"> Delete </Button>
            </div>
        </div>
    </div>
</template>
