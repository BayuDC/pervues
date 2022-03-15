<script>
import BookCard from './BookCard.vue';
import Button from './Button.vue';
import Input from './Input.vue';

export default {
    name: 'BookForm',
    components: { Input, Button, BookCard },
    method: {
        submit() {},
    },
};
</script>

<template>
    <form @submit.prevent="submit">
        <BookCard>
            <template #default>
                <Input name="Title" />
                <Input name="Author" />
            </template>
            <template #btn-group>
                <Button type="success" size="small">Save</Button>
            </template>
        </BookCard>
    </form>
</template>
