<script>
import BookCard from "./BookCard.vue";
import Button from "./Button.vue";
import Input from "./Input.vue";

export default {
    name: "BookForm",
    components: { Input, Button, BookCard },
    props: ["book"],
    methods: {
        onSubmit() {
            this.$emit("save", {
                id: this.book?.id,
                title: this.title,
                author: this.author,
            });
            this.title = this.author = "";
        },
    },
    data() {
        return {
            title: this.book?.title || "",
            author: this.book?.author || "",
        };
    },
};
</script>

<template>
    <form @submit.prevent="onSubmit">
        <BookCard>
            <template #default>
                <h5 class="card-title">
                    <template v-if="this.book">Edit Book</template>
                    <template v-else>Add Book</template>
                </h5>

                <Input v-model="title" label="Title" name="title" />
                <Input v-model="author" label="Author" name="author" />
            </template>
            <template #btn-group>
                <Button type="success" size="small">Save</Button>
            </template>
        </BookCard>
    </form>
</template>
