<template>
  <div class="container">
    <div class="slider">
      <button @click="next" class="next">
          <i class="fas fa-arrow-left"></i>
        </button>
    <div class="info-bottom" id="slide">
      <div class="card" v-for="(item, index) in items" :key="index">
        <div class="imgBox">
          <img class="image" style="width:100%" :src="item.src" alt="product image">
        </div>
      </div>
    </div>
      <button @click="previous" class="prev">
          <i class="fas fa-arrow-right"></i>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CompanySlider',
  data () {
    return {
      count: 0,
      items: [
        {
          src: require('../../assets/prof-1.png')
        },
        {
          src: require('../../assets/prof-2.png')
        },
        {
          src: require('../../assets/prof-3.png')
        },
        {
          src: require('../../assets/prof-4.png')
        },
        {
          src: require('../../assets/prof-5.png')
        }
      ],
      frame: 2
    }
  },
  methods: {
    next () {
      this.count--
      this.scroll('previous')
    },
    previous () {
      this.count++
      this.scroll('next')
    },
    scroll (position) {
      const el = document.getElementById('slide')
      let pos = 0
      const id = setInterval(frame, 5)
      const num = this.items.length - this.frame
      const width = 250
      const resize = num * width
      const check = position === 'reset' ? resize : width
      function frame () {
        if (pos === check) {
          clearInterval(id)
        } else {
          pos += 5
          if (position === 'next') {
            el.scrollLeft += 5
          } else {
            el.scrollLeft -= 5
          }
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  margin-bottom: 30px;
  #slide {
    display: flex;
    overflow: hidden;
    justify-content: space-between;
    align-items: flex-start;
  }
  .slider {
    width: 770px;
    margin-top: 20px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    button {
        height: 40px;
        width: 50px;
        top: calc(50% - 20px);
        border: none;
        color: #93c0dc;
        background: none;
      }
      button:focus,
      button:hover {
        outline: none;
        cursor: pointer;
      }
    .info-bottom {
      width: 700px;
      margin: 30px 0;
      display: flex;
      justify-self: center;
      align-self: center;
      flex-flow: row nowrap;
      .card {
        .imgBox {
          width: 220px;
          .image {
            width: 100px;
            height: 60px;
          }
        }
      }
    }
  }
}
@media (max-width: 1024px) {
  .container {
    width: 100%;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    margin-bottom: 30px;
    #slide {
      display: flex;
      overflow: hidden;
      justify-content: space-between;
      align-items: flex-start;
    }
    .slider {
      width: 300px;
      margin-top: 20px;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      button {
          height: 40px;
          width: 50px;
          top: calc(50% - 20px);
          border: none;
          color: #93c0dc;
          background: none;
        }
        button:focus,
        button:hover {
          outline: none;
          cursor: pointer;
        }
      .info-bottom {
        width: 250px;
        margin: 30px 0;
        display: flex;
        justify-self: center;
        align-self: center;
        flex-flow: row nowrap;
        .card {
          .imgBox {
            width: 180px;
            .image {
            }
          }
        }
      }
    }
  }
}
</style>
