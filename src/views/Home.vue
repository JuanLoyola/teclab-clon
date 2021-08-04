<template>
  <div class="home">
    <BannerOne />
    <Careers />
    <RoadMap />
    <BannerTwo />
  </div>
</template>

<script>
import BannerOne from '@/components/BannerOne.vue'
import Careers from '@/components/Careers.vue'
import RoadMap from '@/components/RoadMap.vue'
import BannerTwo from '@/components/BannerTwo.vue'

export default {
  name: 'Home',
  components: {
    BannerOne,
    Careers,
    RoadMap,
    BannerTwo
  }
}
</script>
