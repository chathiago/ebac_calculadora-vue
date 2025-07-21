<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue']
}
</script>

<template>
    <div class="d-block mb-4">
        <select class="form-select" :v-model="modelValue" @change="$emit('update:modelValue', $event.target.value)">
            <option selected value="+" @select="$emit('update:modelValue', '+')">+</option>
            <option value="-" @select="$emit('update:modelValue', '-')">-</option>
            <option value="x" @select="$emit('update:modelValue', 'x')">x</option>
            <option value="/" @select="$emit('update:modelValue', '/')">/</option>
        </select>

        <!-- <button class="fw-bold btn btn-outline-primary me-2" @click="$emit('update:modelValue', '+')">+</button>
        <button class="fw-bold btn btn-outline-primary me-2" @click="$emit('update:modelValue', '-')">-</button>
        <button class="fw-bold btn btn-outline-primary me-2" @click="$emit('update:modelValue', 'x')">x</button>
        <button class="fw-bold btn btn-outline-primary" @click="$emit('update:modelValue', '/')">/</button> -->
    </div>
</template>

<style scoped>
    .form-select {
        width: 200px;
        margin: 0 auto;
        color: cornflowerblue;
        border-color: cornflowerblue;
    }

    .form-select:focus {
        color: cornflowerblue;
        font-weight: bold;
    }
</style>