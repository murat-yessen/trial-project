<template>
  <div id="app">
    <RealEstate />
    <Info />
  </div>
</template>

<script>
import RealEstate from "@/components/RealEstate.vue";
import Info from "@/components/Info.vue";

export default {
  name: "App",
  components: {
    RealEstate,
    Info,
  },
};
</script>

<style lang="scss">
#app {
  font-size: inherit;
}
</style>
