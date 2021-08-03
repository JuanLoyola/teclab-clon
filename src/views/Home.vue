<template>
  <div class="home">
    <BannerOne />
    <Careers />
  </div>
</template>

<script>
import BannerOne from '@/components/BannerOne.vue'
import Careers from '@/components/Careers.vue'

export default {
  name: 'Home',
  components: {
    BannerOne,
    Careers
  }
}
</script>
