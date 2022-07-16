<script setup>
import Project from "./items/ProjectItem.vue";
</script>

<template>
  <div>
    <h2 class="divider">Projects</h2>
    <Project
      repository="Module"
      description="Multipurporse Discord bot written on Java and Spring."
    />
    <Project
      repository="HCWeb"
      description="A simple blog with authorization, registration, account management and admin panel."
    />
    <Project
      repository="Module-Web"
      description="Website for Module written on Vue.JS. Deprecated!"
    />
    <Project
      repository="EclipseAndroid"
      description="The Dashboard on Android for the bot with name Eclipse by Night Devs"
    />
    <Project
      repository="Knight"
      description="Chess social network written on Kotlin and Ktor."
    />
  </div>
</template>
