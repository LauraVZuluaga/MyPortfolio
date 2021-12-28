<template>
  <div>
    <app-home-portfolio></app-home-portfolio>
  </div>
</template>

<script>
// @ is an alias to /src
import AppHomePortfolio from "@/components/AppHomePortfolio.vue";

export default {
  name: "Home",
  components: {
    AppHomePortfolio,
  },
};
</script>
