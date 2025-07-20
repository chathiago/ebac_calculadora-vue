<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue']
}
</script>

<template>
    <div class="d-block mb-4">
        <button class="fw-bold btn fw-bold btn-outline-primary me-2" @click="$emit('update:modelValue', '+')">+</button>
        <button class="fw-bold btn fw-bold btn-outline-primary me-2" @click="$emit('update:modelValue', '-')">-</button>
        <button class="fw-bold btn fw-bold btn-outline-primary me-2" @click="$emit('update:modelValue', 'x')">x</button>
        <button class="fw-bold btn fw-bold btn-outline-primary" @click="$emit('update:modelValue', '/')">/</button>
    </div>
</template>