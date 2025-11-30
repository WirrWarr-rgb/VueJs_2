<script setup>
const model = defineModel();
defineProps({
  placeholder: {
    type: String,
    default: '',
  },
});
</script>

<template>
  <textarea v-model="model" :placeholder="placeholder" class="form-control" rows="4"></textarea>
</template>
