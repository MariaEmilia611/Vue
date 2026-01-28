<template>
    <div class="buttons">
        <MyButton 
         title="Soma"
         @updated="$emit('change-count', 'increment', 1)"
        />
        <MyButton 
         title="Subtração" 
          @updated="$emit('change-count', 'decrement', 1)"

        />
        <MyButton 
         title="Resetar"    
          @updated="$emit('change-count', 'reset')"
        />
    </div>
</template>

<script>
import MyButton from './MyButton.vue';
export default {
    name: 'CounterButtons',
    emits: ['change-count'],
    components: {
        MyButton
    }
}
</script>

<style>
.buttons {
    display: flex;
    gap: 10px;
}
</style>