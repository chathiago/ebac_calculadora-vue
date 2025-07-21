<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue'],
}
</script>

<template>
    <input class="form-control mb-4" type="number" :value="modelValue" @input="$emit('update:modelValue', parseFloat($event.target.value))" />
</template>

<style scoped>
    .form-control {
        width: 200px;
        margin: 0 auto;
        color: cornflowerblue;
        border-color: cornflowerblue;
    }

    .form-control:focus {
        color: cornflowerblue;
        font-weight: bold;
    }
</style>