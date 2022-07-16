<script setup>
import ReferenceItem from "./items/ReferenceItem.vue";
</script>

<template>
  <div class="link-array">
    <h2>References</h2>
    <ReferenceItem url="discord.com/users/873180556018450512" name="Discord" />
    <ReferenceItem url="github.com/HeadcrabJ" name="Github" />
    <ReferenceItem url="steamcommunity.com/id/headcrabj" name="Steam" />
  </div>
</template>

<style>
.link-array a {
  margin: 8px;
}
</style>
