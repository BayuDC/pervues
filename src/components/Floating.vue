<script>
export default {
    name: "Floating",
};
</script>

<template>
    <div class="fixed-bottom">
        <div class="container py-4 d-flex justify-content-end">
            <slot />
        </div>
    </div>
</template>