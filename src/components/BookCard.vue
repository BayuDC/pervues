<script>
import Button from "./Button.vue";
import BookInfo from "./BookInfo.vue";

export default {
    name: "BookCard",
    props: ["book"],
    components: {
        Button,
        BookInfo,
    },
};
</script>
<template>
    <div class="card border-dark mb-3">
        <div class="card-body">
            <BookInfo :title="book.title" :author="book.author" />
            <div class="d-flex justify-content-end gap-1 pt-4">
                <Button type="primary" size="small">Update</Button>
                <Button type="danger" size="small">Delete</Button>
            </div>
        </div>
    </div>
</template>