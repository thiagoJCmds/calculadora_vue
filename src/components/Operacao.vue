<script setup>
    const props = defineProps(['operacao', 'num1', 'num2'])
</script>

<template>
    <div class="operation">
        <h2> Selecione a operação aritimética desejada</h2>
        <select @change="props.operacao">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
    </div>
    <div>
        <input @keyup="props.num1" required type="number" placeholder="digite o primeiro valor">
        <input @keyup="props.num2" required type="number" placeholder="digite o segundo valor">
    </div>
</template>

<style scoped>
    input{
        margin: 30px;
        padding: 4px;
        border-radius: 4px;
    }
</style>