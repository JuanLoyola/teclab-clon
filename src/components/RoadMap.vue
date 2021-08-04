<template>
  <div class="container">
    <h2 class="container-title">Teclab, Educaci&oacute;n para cambiarlo todo</h2>
    <h4 class="container-info">Asumimos el desafío de crear, iterar, aprender y enseñar diferente, pensando en vos. Para que cambies lo que quieras, tu trabajo, tu carrera, tu futuro, tus oportunidades, nosotros diseñamos lo que el mundo profesional y laboral necesitan: educación para cambiarlo todo.</h4>
    <div class="col">
      <LeftArrow
        :style= "{color: '#44b5a6'}"
        img="step1.png"
        title="Co-creamos carreras con expertos"
        info="Aprendé de los que ejercen. Todas nuestras carreras son co-creadas con expertos de la industria."
      />
      <RightArrow
        :style= "{color: '#acb538'}"
        img="step2.png"
        title="Somos Digitales"
        info="Adaptamos la educación a la nueva realidad digital para que puedas destacarte en el mundo productivo de hoy y de mañana."
      />
      <LeftArrow
        :style= "{color: '#d34b3b'}"
        img="step3.png"
        title="Educación por tramos"
        info="En 2 años recibís el título de tu Tecnicatura Superior avalada por el Ministerio de Educación y, además, contás con un Certificado Intermedio Oficial luego del primer año de cursado."
      />
      <RightArrow
        :style= "{color: '#61bccc'}"
        img="step4.png"
        title="Carreras pensadas 100% online"
        info="Vos administrás tus horas de estudio y elegís desde dónde estudiar y cuando rendir de forma remota."
      />
    </div>
  </div>
</template>

<script>
import LeftArrow from '@/components/roadmap/LeftArrow.vue'
import RightArrow from '@/components/roadmap/RightArrow.vue'

export default {
  name: 'RoadMap',

  components: {
    LeftArrow,
    RightArrow
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  background: #fff;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;

  &-title {
    font-size: 2.1rem;
    color: #68776c;
    margin-top: 50px;
  }

  &-info {
    width: 630px;
    font-size: 1rem;
    font-weight: 500;
    text-align: start;
    color: #999999;
    word-break: break-word;
    margin-top: 10px;
  }

  .col {
    width: 1060px;
    height: 780px;
  }
}

@media (max-width: 780px) {
  .container {

    &-title {
      font-size: 1.3rem;
      color: #68776c;
    }

    &-info {
      width: 220px;
      font-size: 0.9rem;
    }

    .col {
      width: 100%;
      height: 740px;
    }
  }
}
</style>
