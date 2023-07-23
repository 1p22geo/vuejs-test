<script setup>
defineProps(['href', 'title'])
</script>
<template>
  <NuxtLink class="link" :to="href"> {{ title }}</NuxtLink>
</template>