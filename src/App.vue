<template>
  <div id="app">
    <NewObjects />
    <RealEstate />
    <Info />
    <Category />
    <Reviews />
    <Videos />
    <News />
    <Footer />
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
import Footer from "@/components/Footer.vue";

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
    Footer,
  },
};
</script>

<style lang="scss">
#app {
  font-size: inherit;
}
</style>
