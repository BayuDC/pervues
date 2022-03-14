<script>
export default {
    name: "Button",
    props: ["type", "size"],
};
</script>

<template>
    <button
        class="btn"
        :class="{
            'btn-primary': type == 'primary',
            'btn-success': type == 'success',
            'btn-danger': type == 'danger',
            'btn-sm': size == 'small',
            'btn-lg': size == 'large',
        }"
    >
        <slot />
    </button>
</template>