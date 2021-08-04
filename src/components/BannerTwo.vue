<template>
  <div class="container">
    <MiniBannerOne
    title="Seguro de adaptación"
    info="En la educación superior Argentina, las tasas más altas de deserción se dan en el primer cuatrimestre de cursado. En Teclab lo entendemos y sabemos que, para alcanzar tu meta, te tenés que adaptar a la modalidad."
    />
    <MiniBannerTwo
    title="Articulación con Universidad Siglo 21"
    info="Para nosotros es muy importante que puedas seguir con tu proceso de formación."
    />
  </div>
</template>

<script>
import MiniBannerOne from '@/components/information/MiniBannerOne.vue'
import MiniBannerTwo from '@/components/information/MiniBannerTwo.vue'

export default {
  name: 'BannerTwo',

  components: {
    MiniBannerOne,
    MiniBannerTwo
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 50vh;
  background: #fff;
  padding: 30px 0;
}

</style>
