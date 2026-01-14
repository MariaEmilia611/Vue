<template>
    <button @click="$emit('increment')">
        +1
    </button>
</template>
<script>
    export default {
        name: 'MyButton',
    }
</script>
<style>
    button {
        padding: 10px;
        background-color: green;
        color: white;
        border: none;
        border-radius: 8px;
        cursor: pointer;
    }
    button:hover {
        background-color: aquamarine;
    }
</style>