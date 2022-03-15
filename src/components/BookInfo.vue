<script>
import BookCard from "./BookCard.vue";
import Button from "./Button.vue";

export default {
    name: "BookInfo",
    props: ["book"],
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
            <Button @click="book.editMode = true" type="primary" size="small">
                Edit
            </Button>
            <Button
                @click="$emit('destroy', book.id)"
                type="danger"
                size="small"
            >
                Delete
            </Button>
        </template>
    </BookCard>
</template>
