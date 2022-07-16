<script>
import ProjectsBlock from "./components/ProjectsBlock.vue";
import ReferencesBlock from "./components/ReferencesBlock.vue";
import SupportUsBlock from "./components/SupportUsBlock.vue";

const screenWidth = 1000;

export default {
  components: { SupportUsBlock, ReferencesBlock, ProjectsBlock },
  data() {
    return {
      isMobile: window.innerWidth < screenWidth,
      y: window.scrollY,
      hintVisible: window.localStorage.getItem("hintVisible") || "1",
    };
  },
  mounted() {
    window.addEventListener("resize", this.checkMobile);
  },
  unmounted() {
    window.removeEventListener("resize", this.checkMobile);
  },
  methods: {
    checkMobile() {
      this.isMobile = window.innerWidth < screenWidth;
    },
    openOneScreen() {
      this.$refs.one.scrollIntoView();
    },
    openTwoScreen() {
      this.$refs.two.scrollIntoView();
      if (this.hintVisible !== "0") {
        this.hintVisible = "0";
        window.localStorage.setItem("hintVisible", "0");
      }
    },
  },
};
</script>

<template>
  <section class="title_container" ref="one" @click="openTwoScreen">
    <h1 class="title" v-if="isMobile">Krabi</h1>
    <h1 class="title" v-else>Headcrab</h1>
    <p class="title_footer" v-if="hintVisible === '1'">Click me</p>
  </section>
  <section class="content" ref="two" @click="openOneScreen">
    <div>
      <ProjectsBlock />
      <ReferencesBlock />
      <SupportUsBlock />
    </div>
  </section>
</template>
