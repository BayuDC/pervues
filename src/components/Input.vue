<script>
export default {
    name: "Input",
    props: ["name", "label", "modelValue"],
};
</script>

<template>
    <div class="mb-2">
        <label :for="name" class="form-labell">{{ label }}</label>
        <input
            @input="$emit('update:modelValue', $event.target.value)"
            :value="modelValue"
            :id="name"
            type="text"
            class="form-control"
            required
        />
    </div>
</template>
