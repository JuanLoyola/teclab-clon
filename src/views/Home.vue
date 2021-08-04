<template>
  <div class="home">
    <BannerOne />
    <Careers />
    <RoadMap />
  </div>
</template>

<script>
import BannerOne from '@/components/BannerOne.vue'
import Careers from '@/components/Careers.vue'
import RoadMap from '@/components/RoadMap.vue'

export default {
  name: 'Home',
  components: {
    BannerOne,
    Careers,
    RoadMap
  }
}
</script>
