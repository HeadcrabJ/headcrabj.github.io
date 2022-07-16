<script setup>
import ProjectBlock from "./components/ProjectsBlock.vue";
import ReferencesBlock from "./components/ReferencesBlock.vue";
import SupportUsBlock from "./components/SupportUsBlock.vue";
</script>

<template>
  <div class="title_container">
    <h1 class="title">Headcrab</h1>
  </div>
  <div class="content">
    <div>
      <ProjectBlock />
      <ReferencesBlock />
      <SupportUsBlock />
    </div>
  </div>
</template>
