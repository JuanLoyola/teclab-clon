<template>
  <div class="home">
    <BannerOne />
    <Careers />
    <RoadMap />
    <BannerTwo />
    <Students />
    <Internships />
    <TheFooter />
  </div>
</template>

<script>
import BannerOne from '@/components/BannerOne.vue'
import Careers from '@/components/Careers.vue'
import RoadMap from '@/components/RoadMap.vue'
import BannerTwo from '@/components/BannerTwo.vue'
import Students from '@/components/Students.vue'
import Internships from '@/components/Internships.vue'
import TheFooter from '@/components/TheFooter.vue'

export default {
  name: 'Home',
  components: {
    BannerOne,
    Careers,
    RoadMap,
    BannerTwo,
    Students,
    Internships,
    TheFooter
  }
}
</script>
