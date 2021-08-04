<template>
  <div class="content">
  <div class="background"></div>
    <h2 class="title">Seguro de adaptación</h2>
    <p class="info">En la educación superior Argentina, las tasas más altas de deserción se dan en el primer cuatrimestre de cursado. En Teclab lo entendemos y sabemos que, para alcanzar tu meta, te tenés que adaptar a la modalidad.</p>
    <button class="button">Ver más</button>
  </div>
</template>

<script>
export default {
  name: 'MiniBannerTwo'
}
</script>

<style lang="scss" scoped>
.content {
  width: 100%;
  height: 350px;
  top: 0;
  left: 0;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  line-height: 70px;
  align-items: center;
  color: #fff;
  background: #bdc552;
  z-index: 1;

  .background {
    width: 100%;
    height: 350px;
    top: 0;
    left: 0;
    position: absolute;
    background-image: url('../../assets/bg-3.jpg');
    opacity: .2;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    z-index: -1;
  }
  .title {
    font-size: 2.3rem;
  }

  .info {
    width: 610px;
    line-height: 30px;
    text-align: start;
  }

  .button {
    width: 150px;
    height: 50px;
    margin-top: 30px;
    background: none;
    color: #fff;
    font-weight: 700;
    border: 2px solid #fff;
    border-radius: 5px;
    cursor: pointer;
  }
}

@media (max-width: 780px) {
  .content {
    .title {
      font-size: 1.3rem;
    }

    .info {
      width: 300px;
      line-height: 30px;
      text-align: start;
    }

    .button {
      width: 150px;
      height: 50px;
      margin-top: 30px;
      background: none;
      color: #fff;
      font-weight: 700;
      border: 2px solid #fff;
      border-radius: 5px;
      cursor: pointer;
    }
  }
}
</style>
