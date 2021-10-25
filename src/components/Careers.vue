<template>
  <div class="container">
    <h2 class="container-title">¡Ahora vos tambi&eacute;n pod&eacute;s estudiar una carrera oficial!</h2>
    <h4 class="container-subtitle">Eleg&iacute; entre 12 carreras cortas con salida laboral.</h4>
    <div class="container-cards">
      <div
        class="card"
        v-for="(item, index) in cards.items[0].variants"
        :key="index"
        >
        <img class="img" loading="lazy" width="100%" height="230px" :src=item.img alt="carrera">
        <div class="text">
          <p class="epigraph">Inscripciones abiertas</p>
          <p class="career">{{ item.title }}</p>
          <p class="info">
            Resolución 4519/17 del Ministerio de Educación de la Ciudad de Buenos Aires.
          </p>
        </div>
        <button class="btn">Más información</button>
      </div>
    </div>

    <button class="btn-careers">Ver todas las carreras</button>
  </div>
</template>

<script>
export default {
  name: 'Careers',

  data () {
    return {
      cards: {
        items: [
          {
            variants: [
              {
                img: require('@/assets/careers/careers-1.jpg'),
                title: 'Técnico Superior en Programación'
              },
              {
                img: require('@/assets/careers/careers-2.png'),
                title: 'Técnico Superior en Cloud Administration'
              },
              {
                img: require('@/assets/careers/careers-3.png'),
                title: 'Técnico Superior en Seguridad Informática'
              },
              {
                img: require('@/assets/careers/careers-4.jpg'),
                title: 'Técnico Superior en Gestión Contable'
              }
            ]
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 50px 0 50px 0;

  &-title {
    color: #2782bb;
    text-align: center;
    font-size: 1.5rem;
  }
  &-subtitle {
    font-weight: 500;
    text-align: center;
    margin-top: 20px;
  }

  &-cards {
    width: 100%;
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-content: center;
    margin: 30px 0px;

    .card {
      background: #fff;
      width: 230px;
      height: 450px;
      border-radius: 9px;
      display: flex;
      flex-direction: column;
      justify-content:space-between;
      align-items: center;
      margin-right: 30px;
      border: 1px solid #ccc;
      -webkit-box-shadow: 0px 3px 5px 0px #ccc;
      -moz-box-shadow: 0px 3px 5px 0px #ccc;
      box-shadow: 0px 3px 5px 0px #ccc;

      .img {
        width: 100%;
        height: 230px;
      }

      .text {
        height: 150px;
        text-align: start;
        display: flex;
        flex-direction: column;
        justify-content:space-evenly;
        padding: 0 20px;

        .epigraph {
          font-size: 0.7rem;
          font-weight: 600;
          text-transform: capitalize;
          color: #9ebdce;
        }

        .career {
          font-size: 0.8rem;
          font-weight: 600;
        }

        .info {
          font-size: 0.66rem;
          font-weight: 500;
          color: #929191;
        }
      }

      .btn {
        text-align: center;
        margin: 20px;
        width: 150px;
        height: 40px;
        border-radius: 5px;
        background: #2782bb;
        color: #fff;
        border: none;
        cursor: pointer;
      }

      .btn:hover {
        background: #87cefa;
      }
    }
  }
  .btn-careers {
    text-align: center;
    margin: 20px;
    width: 320px;
    padding: 15px 0;
    border-radius: 5px;
    background: #2782bb;
    color: #fff;
    border: none;
    cursor: pointer;
  }

  .btn-careers:hover {
    background: #87cefa;
  }
}

@media (max-width: 780px) {
  .container {
    height: 100%;

    &-title {
      font-size: 1.2rem;
    }

    &-cards {
      flex-flow: column nowrap;
      align-items: center;

      .card {
        margin-right: 0px;
        margin-top: 20px;
      }
    }
  }
}
</style>
