<script setup>
defineProps({
  repository: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <p>
    <a :href="'https://github.com/HeadcrabJ/' + repository">Module</a> -
    {{ description }}
  </p>
</template>
