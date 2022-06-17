<template>
  <div id="app">
    <NewObjects />
    <RealEstate />
    <Info />
    <Category />
    <Reviews />
    <Videos />
    <News />
  </div>
</template>

<script>
import NewObjects from "@/components/NewObjects.vue";
import RealEstate from "@/components/RealEstate.vue";
import Info from "@/components/Info.vue";
import Videos from "@/components/Videos.vue";
import News from "@/components/News.vue";
import Category from "@/components/Category.vue";
import Reviews from "@/components/Reviews.vue";

export default {
  name: "App",
  components: {
    NewObjects,
    RealEstate,
    Info,
    Category,
    Reviews,
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
