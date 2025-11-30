<script setup>
import TeamCard from './TeamCard.vue';

defineProps({
  peoples: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section class="barista-section section-padding section-bg" id="barista-team">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-12 col-12 text-center mb-4 pb-lg-2">
          <em class="text-white">Creative Baristas</em>
          <h2 class="text-white">Meet People</h2>
        </div>

        <TeamCard v-for="people in peoples" :key="people.name + people.tag" :people="people" />
      </div>
    </div>
  </section>
</template>
