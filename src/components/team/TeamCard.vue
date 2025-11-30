<script setup>
defineProps({
  people: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="col-lg-3 col-md-6 col-12 mb-4">
    <div class="team-block-wrap">
      <div class="team-block-info d-flex flex-column">
        <div class="d-flex mt-auto mb-3">
          <h4 class="text-white mb-0">{{ people.name }}</h4>
          <p class="badge ms-4">
            <em>{{ people.tag }}</em>
          </p>
        </div>
        <p class="text-white mb-0">{{ people.tagline }}</p>
      </div>
      <div class="team-block-image-wrap">
        <img :src="people.image" class="team-block-image img-fluid" alt="" />
      </div>
    </div>
  </div>
</template>
