<template>
  <div class="about">
    <create-grid />
    <challenge />
  </div>
</template>

<script>
import createGrid from "@/components/about/createGrid.vue";
import challenge from "@/components/about/challenge.vue";
export default {
  name: "about",
  components: {
    createGrid,
    challenge
  }
};
</script>
