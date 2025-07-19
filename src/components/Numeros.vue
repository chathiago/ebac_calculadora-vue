<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue'],
}
</script>

<template>
    <input type="number" :value="modelValue" @input="$emit('update:modelValue', parseFloat($event.target.value))" />
</template>

<style>
input {
    border-radius: 10px;
    border: 1px solid #2263b9;
    text-align: center;
    color: #2263b9;
}

input:focus {
    outline: none;
    border-color: #2263b9;
}
</style>