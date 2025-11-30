<script setup>
defineProps({
  rating: {
    type: [String, Number],
    required: true,
  },
});

const generateStarsClass = (rating) => {
  const starsClass = [];
  const fullStars = Math.floor(rating);
  const hasHalfStar = rating % 1 >= 0.5;

  for (let i = 0; i < fullStars; i++) {
    starsClass.push('bi-star-fill');
  }

  if (hasHalfStar) {
    starsClass.push('bi-star-half');
  }

  const emptyStars = 5 - fullStars - (hasHalfStar ? 1 : 0);
  for (let i = 0; i < emptyStars; i++) {
    starsClass.push('bi-star');
  }

  return starsClass;
};
</script>

<template>
  <div class="reviews-group ms-auto">
    <i :class="starClass" v-for="(starClass, index) in generateStarsClass(rating)" :key="index"></i>
  </div>
</template>
