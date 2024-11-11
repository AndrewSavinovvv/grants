<script setup>

import HeaderComponent from "@/components/HeaderComponent.vue";
import InfoComponent from "@/components/InfoComponent.vue";
import ProjectsComponent from "@/components/ProjectsComponent.vue";
import NewsComponent from "@/components/NewsComponent.vue";
import QuestionsComponent from "@/components/QuestionsComponent.vue";
</script>

<template>
<HeaderComponent></HeaderComponent>
  <div class="container">
    <InfoComponent></InfoComponent>
  </div>
<ProjectsComponent></ProjectsComponent>
  <div class="container">
    <NewsComponent></NewsComponent>
    <QuestionsComponent></QuestionsComponent>
  </div>
</template>

<style scoped>

</style>