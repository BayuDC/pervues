<script>
import BookCard from './BookCard.vue';
import Button from './Button.vue';
import Input from './Input.vue';

export default {
    name: 'BookForm',
    components: { Input, Button, BookCard },
    props: ['text'],
    method: {
        submit() {},
    },
};
</script>

<template>
    <form @submit.prevent="submit">
        <BookCard>
            <template #default>
                <h5 class="card-title">{{ text }}</h5>

                <Input label="Title" name="title" />
                <Input label="Author" name="author" />
            </template>
            <template #btn-group>
                <Button type="success" size="small">Save</Button>
            </template>
        </BookCard>
    </form>
</template>
