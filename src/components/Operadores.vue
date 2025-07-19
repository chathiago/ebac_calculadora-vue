<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue']
}
</script>

<template>
    <div>
        <button class="btn-button" @click="$emit('update:modelValue', '+')">+</button>
        <button class="btn-button" @click="$emit('update:modelValue', '-')">-</button>
        <button class="btn-button" @click="$emit('update:modelValue', 'x')">x</button>
        <button class="btn-button" @click="$emit('update:modelValue', '/')">/</button>
    </div>
</template>

<style>
.btn-button {
    margin-right: 10px;
    padding: 6px 12px;
    font-weight: bold;
    color: #fff;
    background-color: #2263b9;
    border-radius: 8px;
    border: 1px solid #2263b9;
    transition: all 0.3s ease;
}

.btn-button:hover {
    background-color: #fff;
    border-color: #2263b9;
    color: #2263b9;
    transition: all 0.3s ease;
}
</style>