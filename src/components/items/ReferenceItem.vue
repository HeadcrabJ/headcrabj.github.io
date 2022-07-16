<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
  url: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <a :href="'https://' + url">{{ name }}</a>
</template>
