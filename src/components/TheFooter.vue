<template>
  <div class="container">
    <div class="container-list">
      <img src="@/assets/footer/teclab-logo-footer.png" class="img" alt="logo teclab">
      <a href="tel:+0810 888 9900" class="phone"><span class="fas fa-phone"></span> 0810 88 9900</a>
      <div class="row">
        <span class="socials fab fa-facebook"></span>
        <span class="socials fab fa-linkedin"></span>
        <span class="socials fab fa-instagram"></span>
      </div>
    </div>

    <div class="container-list">
      <h1 class="title">LINKS</h1>
      <p class="option">Carreras</p>
      <p class="option">Acerca de Teclab</p>
      <p class="option">Aspirante</p>
      <p class="option">Contacto</p>
      <p class="option">Alumno</p>
    </div>

    <div class="container-list">
      <h1 class="title">Articulación con</h1>
      <img id="ues21" src="@/assets/footer/ues21-white.png" alt="universidad 21">
      <h1 class="title">Acreditado por</h1>
      <div class="row">
        <img class="ministerios" src="@/assets/footer/acreditacion-ministerio-educacio.png" alt="">
        <img class="ministerios" src="@/assets/footer/ministerios-white.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheFooter',
  setup () {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 278px;
  background-color: #383838;
  color: #99999999;
  line-height: 25.5px;
  font-size: 13px;
  display: flex;
  justify-content: space-around;
  flex-flow: row nowrap;

  &-list {
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
    flex-flow: column;
    padding: 30px;

    .img {
      width: 200px;
      height: 65.72px;
    }

    .phone {
      color: #6eadb6;
      font-size: 24px;
      font-weight: 700;
      line-height: 40px;
      text-decoration: none;
      margin: 15px 0;

      &:hover {
        color: #86c4ce;
      }
    }

    .row {
      width: 100%;
      display: flex;
      justify-content: space-around;

      .socials {
        font-size: 30px;
        line-height: 34px;
      }

      .socials:hover {
        color: #b37ee4;
        cursor: pointer;
      }

      .ministerios {
        width: 150px;
        height: 62px;
      }
    }

    #ues21 {
      width: 125px;
      height: 50px;
    }

    .title {
      font-size: 1rem;
      color: #f1f1f1;
    }

    .option {
      font-weight: 500;

      &:hover {
        cursor: pointer;
        color:#6eadb6;
      }
    }
  }

    &-list:nth-last-child(2) {
      width: 370px;
      border-left: solid 1px #515151;
      border-right: solid 1px #515151;
      display: flex;
      justify-content: center;
      align-items: flex-start;
  }
}

@media screen and (max-width: 1025px) {
    .container {
    width: 100%;
    height: 800px;
    background-color: #383838;
    color: #99999999;
    line-height: 25.5px;
    font-size: 13px;
    display: flex;
    justify-content: space-around;
    flex-flow: column nowrap;

    &-list {
      max-width: 100%;
      display: flex;
      justify-content: space-around;
      align-items: flex-start;
      flex-flow: column;
      padding: 20px;

      .img {
        width: 200px;
        height: 65.72px;
      }

      .phone {
        color: #6eadb6;
        font-size: 24px;
        font-weight: 700;
        line-height: 40px;
        text-decoration: none;
        margin: 15px 0;

        &:hover {
          color: #86c4ce;
        }
      }

      .row {
        width: 24em;
        display: flex;
        justify-content: space-around;

        .socials {
          font-size: 30px;
          line-height: 34px;
        }

        .socials:hover {
          color: #b37ee4;
          cursor: pointer;
        }

        .ministerios {
          width: 150px;
          height: 62px;
        }
      }

      #ues21 {
        width: 125px;
        height: 50px;
      }

      .title {
        font-size: 1rem;
        color: #f1f1f1;
      }

      .option {
        font-weight: 500;

        &:hover {
          cursor: pointer;
          color:#6eadb6;
        }
      }
    }

      &-list:nth-last-child(2) {
        width: 370px;
        border-left: none;
        border-right: none;
        display: flex;
        justify-content: center;
        align-items: flex-start;
    }
  }
}
</style>
