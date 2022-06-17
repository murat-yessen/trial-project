<template>
  <div id="app">
    <RealEstate />
    <Info />
    <Category />
    <Videos />
    <News />
  </div>
</template>

<script>
import RealEstate from "@/components/RealEstate.vue";
import Info from "@/components/Info.vue";
import Videos from "@/components/Videos.vue";
import News from "@/components/News.vue";
import Category from "@/components/Category.vue";

export default {
  name: "App",
  components: {
    RealEstate,
    Info,
    Category,
    Videos,
    News,
  },
};
</script>

<style lang="scss">
#app {
  font-size: inherit;
}
</style>
