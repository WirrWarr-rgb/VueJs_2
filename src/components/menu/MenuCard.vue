<script setup>
defineProps({
  menu: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="col-lg-6 col-12">
    <div class="menu-block-wrap">
      <div class="text-center mb-4 pb-lg-2">
        <em class="text-white">{{ menu.name }}</em>
        <h4 class="text-white">{{ menu.type }}</h4>
      </div>

      <div v-for="item in menu.items" :key="item.name" class="menu-block my-4">
        <div class="d-flex">
          <h6>
            {{ item.name }}
            <span v-if="item.isRecommended" class="badge ms-3">Recommend</span>
          </h6>
          <span class="underline"></span>
          <div class="ms-auto">
            <strong v-if="item.oldPrice" class="text-white ms-auto">
              <s>{{ item.oldPrice }}</s>
            </strong>
            <strong class="ms-2">{{ item.price }}</strong>
          </div>
        </div>
        <div class="border-top mt-2 pt-2">
          <small>{{ item.descr }}</small>
        </div>
      </div>
    </div>
  </div>
</template>
