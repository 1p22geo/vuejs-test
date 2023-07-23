<script setup>
let counter = ref(0)
</script>
<template>
    <div>
        <button @click="counter++">kliknij mnie  {{ counter }}</button>

    </div>
</template>