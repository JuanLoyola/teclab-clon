<template>
  <div class="container">
    <h1 class="title">Nuestros Alumnos</h1>
    <blockquote class="quote">
      <p class="content">
        Mi experiencia con la modalidad online de Teclab es muy buena. Todo lo que estoy aprendiendo ahora lo estoy aplicando en mi lugar de trabajo.
      </p>
      <div class="tip"></div>
    </blockquote>

    <div class="imgBox">
      <a href="https://portfoliov2.hostman.site" target="_blank" rel="noopener noreferrer"><img class="img" src="@/assets/me.jpg" alt="alumno"></a>
    </div>

    <p class="student">Juan - Estudiante de Programación</p>
  </div>
</template>

<script>
export default {
  name: 'Students'
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;
  padding-bottom: 90px;

  .title {
    font-size: 2.5rem;
    margin-top: 90px;
    color: #333;
  }

  .quote {
    position: relative;
    width: 911px;
    background-color: #61bccc;
    color: #fff;
    font-weight: 500;
    border-radius: 9px;
    padding: 20px 20px;
    margin: 60px 0;

    .content {
      padding: 20px;
    }

    .tip::after {
      content: '';
      position: absolute;
      border-left: 1rem solid transparent;
      border-right: 1rem solid transparent;
      border-top: 1rem solid #61bccc;
      top: 100%;
      left: 50%;
      bottom: 1rem;
      transform: translate(-50%);
    }
  }

  .quote::before {
    position: absolute;
    top: 0;
    left: 0;
    content:'\275D';
    color: #fff;
    font-size: 3rem;
    padding: 0 20px;
  }

  .quote::after {
    position: absolute;
    bottom: 0;
    right: 0;
    content:'\275E';
    color: #fff;
    font-size: 3rem;
    padding: 0 20px;
  }

  .imgBox {
    width: 180px;
    height: 180px;
    margin-top: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    background: #5f79a5;
    .img {
      width: 145px;
      border: 3px solid #fff;
      border-radius: 50%;
    }
  }

  .student {
    margin-top: 30px;
    color: #6bc2d7;
    font-size: 1.2rem;
    font-weight: 600;
  }
}

@media (max-width: 780px) {
  .container {
    width: 100%;
    height: 100%;

    .title {
      font-size: 1.5rem;
      color: #333;
    }

    .quote {
      position: relative;
      width: 300px;
      padding: 20px 0;
    }

    .student {
      width: 300px;
    }

  }
}
</style>
