<script setup>
const model = defineModel();
defineProps({
  type: {
    type: String,
    default: 'text',
  },
  placeholder: {
    type: String,
    default: '',
  },
});
</script>

<template>
  <input v-model="model" :type="type" :placeholder="placeholder" class="form-control" />
</template>
