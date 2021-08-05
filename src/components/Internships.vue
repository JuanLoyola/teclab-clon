<template>
  <div class="internships">
    <h2 class="internships-title">Prácticas Profesionalizantes</h2>
    <h5 class="internships-subtitle">Realizá tus prácticas en empresas como estas:</h5>
    <CompanySlider />
  </div>
</template>

<script>
import CompanySlider from '@/components/slider/CompanySlider.vue'

export default {
  name: 'Internships',

  components: {
    CompanySlider
  }
}
</script>

<style lang="scss" scoped>
.internships {
  width: 100%;
  height: 40vh;
  background: #fff;
  color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  &-title {
    font-size: 1.8rem;
    margin-bottom: 20px;
  }

  &-subtitle {
    font-size: 0.9rem;
    font-weight: 500;
  }
}
</style>
