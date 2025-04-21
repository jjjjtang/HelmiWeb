<script setup>

import HeaderComponent from "@/components/homeViewComponents/HeaderComponent.vue";
import ContentComponent from "@/components/homeViewComponents/ContentComponent.vue";
import BodyComponent from "@/components/homeViewComponents/BodyComponent.vue";

</script>

<template>
  <div class="container1">
    <HeaderComponent></HeaderComponent>

    <ContentComponent></ContentComponent>

    <BodyComponent></BodyComponent>

  </div>
</template>

<style scoped>

.container1{
  height:800px;
  width: 100%;
}
</style>