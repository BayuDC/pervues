<script>
export default {
    name: 'BookCard',
};
</script>
<template>
    <div class="card border-dark mb-sm-4 mb-3">
        <div class="card-body">
            <slot />
            <div class="d-flex justify-content-end gap-1 pt-4">
                <slot name="btn-group" />
            </div>
        </div>
    </div>
</template>
