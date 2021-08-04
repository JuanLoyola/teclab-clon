<template>
  <div class="container">
    <div class="right">
      <img class="right-img" :src="require(`@/assets/${img}`)"  alt="explicacion">
      <div class="right-text">
        <h2 class="title">{{ title }}</h2>
        <p class="info">{{ info }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RightArrow',

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
  min-height: 150px;
  display: flex;
  .right {
    width: 90%;
    min-height: 150px;
    margin-bottom: 30px;
    text-align: start;
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    flex-flow: row-reverse nowrap;

    &-img {
      width: 80px;
      height: 90px;
      margin-left: 15px;
    }

    &-text {
      display: flex;
      flex-direction: column;
      text-align: end;
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
    .right {
      justify-content: center;
      &-img {
        width: 80px;
        height: 90px;
        margin-left: 5px;
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
