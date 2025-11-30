<script setup>
import MenuCard from './MenuCard.vue';

defineProps({
  menus: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section class="menu-section section-padding" id="section_3">
    <div class="container">
      <div class="row">
        <MenuCard v-for="menu in menus" :key="menu.name + menu.type" :menu="menu" />
      </div>
    </div>
  </section>
</template>
