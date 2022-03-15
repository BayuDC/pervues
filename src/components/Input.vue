<script>
export default {
    name: 'Input',
    props: ['name'],
};
</script>

<template>
    <div class="mb-2">
        <label :for="name" class="form-labell">{{ name }}</label>
        <input type="text" :id="name" class="form-control" required />
    </div>
</template>
