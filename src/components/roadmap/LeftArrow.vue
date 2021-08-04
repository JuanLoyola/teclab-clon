<template>
  <div class="container">
    <div class="left">
      <img class="left-img" :src="require(`@/assets/${img}`)"  alt="explicacion">
      <div class="left-text">
        <h2 class="title">{{ title }}</h2>
        <p class="info">{{ info }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LeftArrow',

  props: {
    img: String,
    title: String,
    info: String,
    color: String
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  min-height: 180px;
  margin-top: 10px;
  display: flex;
  align-items: flex-end;
  .left {
    width: 90%;
    text-align: start;
    display: flex;
    align-items: center;
    flex-flow: row nowrap;

    &-img {
      width: 80px;
      height: 90px;
      margin-right: 15px;
    }

    &-text {
      display: flex;
      flex-direction: column;
      margin-top: 30px;
      .title {
        font-size: 1.8rem;
      }

      .info {
        width: 420px;
        margin-top: 10px;
        color: #817f7f;
      }
    }
  }
}

@media (max-width: 780px) {
  .container {
    justify-content: center;
    align-items: center;
    .left {
      justify-content: center;
      &-img {
        width: 80px;
        height: 90px;
        margin-right: 5px;
      }

      &-text {
        .title {
          font-size: 1.2rem;
        }

        .info {
          width: 300px;
          margin-top: 10px;
          color: #817f7f;
        }
      }
    }
  }
}
</style>
