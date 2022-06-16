<template>
  <div id="app">
    <RealEstate />
    <Info />
    <Videos />
  </div>
</template>

<script>
import RealEstate from "@/components/RealEstate.vue";
import Info from "@/components/Info.vue";
import Videos from "@/components/Videos.vue";

export default {
  name: "App",
  components: {
    RealEstate,
    Info,
    Videos,
  },
};
</script>

<style lang="scss">
#app {
  font-size: inherit;
}
</style>
