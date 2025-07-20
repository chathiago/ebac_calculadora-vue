<script>
export default {
    props: ['valor1', 'valor2', 'operacao'],
    computed: {
        resultado() {
            if (isNaN(parseFloat(this.valor1)) || isNaN(parseFloat(this.valor2))) {
                return '...';
            }

            const v1 = parseFloat(this.valor1);
            const v2 = parseFloat(this.valor2);

            switch (this.operacao) {
                case '+': return v1 + v2;
                case '-': return v1 - v2;
                case 'x': return v1 * v2;
                case '/':
                    if (v2 === 0) {
                        return 'Ops! Isso é uma divisão por zero.';
                    }
                    const resDivisao = v1 / v2;
                    return Number.isInteger(resDivisao) ? resDivisao : resDivisao.toFixed(2);
                default: return '0';
            }
        }
    }
}
</script>

<template>
    <span class="fw-bold">{{ resultado }}</span>
</template>

<style>
    span {
        color: cornflowerblue;
        font-size: 1.5rem;
    }
</style>