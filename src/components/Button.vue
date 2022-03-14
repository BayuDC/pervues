<script>
export default {
    name: "Button",
    props: ["type"],
};
</script>

<template>
    <button
        class="btn btn-sm"
        :class="{
            'btn-primary': type == 'primary',
            'btn-success': type == 'success',
            'btn-danger': type == 'danger',
        }"
    >
        <slot />
    </button>
</template>