<script>
import Input from './Input.vue';
export default {
    name: 'BookForm',
    components: { Input },
    method: {
        submit() {},
    },
};
</script>

<template>
    <form @submit.prevent="submit">
        <Input name="Title" />
        <Input name="Author" />
    </form>
</template>
