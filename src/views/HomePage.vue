<template>
  <div class="homepage">
    <AsideLeft />
    <TabsMenu />
    <TrackNav />
    <AsideRight />
    <Hero />
    <Playlists />
    <LatestSection />
    <FansAlsoLike />
  </div>
</template>


<script>
import AsideLeft from "../components/AsideLeft.vue";
import AsideRight from "../components/AsideRight.vue";
import TrackNav from "../components/TrackNav.vue";
import Hero from "../components/Hero.vue";
import TabsMenu from "../components/TabsMenu.vue";
import Playlists from "../components/Playlists.vue";
import LatestSection from "../components/LatestSection.vue";
import FansAlsoLike from "../components/FansAlsoLike.vue";

export default {
  components: {
    AsideLeft,
    TrackNav,
    AsideRight,
    Hero,
    TabsMenu,
    Playlists,
    LatestSection,
    FansAlsoLike,
  },
};
</script>


<style>
.homepage {
  width: 1366px;
  left: -700px;
  top: 34px;

  background: #0a0a0a;
  border: 0.01px solid black;
  height: 768px;
}
template {
  background: #0a0a0a;
}
</style>
