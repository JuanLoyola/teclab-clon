<template>
  <div class="container">
    <div class="container_center">
      <div class="container_center-text">
        <h2 class="title">¡Aprend&eacute; de los que ejercen!</h2>
        <div class="info">
          <p>12 carreras de 2 años de duracion, co-creadas con expertos de la industria y con Titulo Oficial. Estamos conectados con vos, porque eso es lo que necesitás.</p>
        </div>
        <div class="inscription">¡Inscribite hoy!</div>
      </div>
      <div class="container_center-form">
        <form>
          <h2 class="title">Complet&aacute; el formulario y obten&eacute; m&aacute;s informaci&oacute;n</h2>
          <div class="form-tag">
            <label class="label" for="careers">Carrera <span class="important">*</span></label>
            <select class="input" type="text" name="careers">
              <option value="Buenos aires">Programación</option>
              <option value="Buenos aires">Contabilidad</option>
              <option value="Buenos aires">Diseño</option>
            </select>
          </div>
          <div class="form-tag">
            <label class="label" for="careers">Provincia <span class="important">*</span></label>
            <select class="input" type="text" name="careers">
              <option value="Buenos aires">Buenos Aires</option>
              <option value="Buenos aires">Cordoba</option>
              <option value="Buenos aires">Santa Fe</option>
              <option value="Buenos aires">San Luis</option>
              <option value="Buenos aires">Formosa</option>
            </select>
          </div>
          <div class="form-tag">
            <label class="label" for="careers">Nombre <span class="important">*</span></label>
            <input class="input" type="text" name="careers" placeholder="">
          </div>
          <div class="form-tag">
            <label class="label" for="careers">Correo <span class="important">*</span></label>
            <input class="input" type="email" name="careers" placeholder="">
          </div>
          <div class="form-tag">
            <label class="label" for="careers">Número de celular <span class="important">*</span></label>
            <input class="input" type="number" name="careers" placeholder="">
          </div>
          <div class="form-tag">
            <label class="label" for="careers">Franja Horaria <span class="important">*</span></label>
            <select class="input" type="text" name="careers">
              <option value="Buenos aires">Mañana</option>
              <option value="Buenos aires">Tarde</option>
              <option value="Buenos aires">Noche</option>
            </select>
          </div>
          <a href="#" class="btn">Enviar</a>

        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BannerOne'
}
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100vh;
  background: url('../assets/bg-1.jpg') no-repeat center center / cover;
  margin-top: -70px;
  border-radius: 0 0 16em 0;

  &_center {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: space-evenly;
    align-items: center;

    &-text {
      width: 480px;
      height: 200px;
      color: #fff;
      text-align: start;
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;

      .title {
        font-size: 1.7rem;
        font-weight: 500;
        text-transform: uppercase;
      }

      .info {
        font-size: 1.1rem;
      }

      .inscription {
        font-weight: 500;
        text-transform: uppercase;
      }
    }

    &-form {
      width: 300px;
      height: 480px;
      background: #fff;
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 8em;
      border-radius: 9px;
      -webkit-box-shadow: 0px 3px 5px 0px #686565;
      -moz-box-shadow: 0px 3px 5px 0px #686565;
      box-shadow: 0px 3px 5px 0px #686565;

      .title {
        color: #4682b4;
        font-size: 0.9rem;
        font-weight: 600;
        text-align: start;
        padding: 10px 20px;
      }

      .form-tag {
        width: 260px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        margin:0 20px 10px 20px;

        .label {
          font-size: 0.7rem;
          font-weight: 600;
          margin-bottom: 5px;
          .important {
            color: #ff0000;
            font-weight: bold;
          }
        }

        .input {
          width: 260px;
          height: 30px;
          border: 1px solid #ccc;
          padding: 5px 10px;
          transition: 0.4s;
        }
      }

      .btn {
        background: blueviolet;
        color: #fff;
        font-size: 0.8rem;
        text-transform: uppercase;
        text-decoration: none;
        padding: 5px 30px;
        border-radius: 5px;
        transition: linear 0.5s;
      }

      .btn:hover {
        background: lightskyblue;
      }
    }
  }
}

@media (max-width: 780px) {
  .container {
    width: 100%;
    height: 800px;
    margin-top: 0px;

    &_center {
      width: 100%;
      height: 100vh;
      display: flex;
      flex-direction: column;
      padding-top: 8em;

      &-text {
        width: 300px;
        height: 200px;
        text-shadow: 1px 1px 1px #333;

        .title {
          font-size: 1rem;
          font-weight: 500;
          text-transform: uppercase;
        }

        .info {
          font-size: 0.9rem;
          margin: 8px 0;
        }

        .inscription {
          font-weight: 500;
          text-transform: uppercase;
        }
      }

      &-form {
        width: 300px;
        height: 480px;
        background: #fff;
        color: #333;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 8em;
        border-radius: 9px;
        -webkit-box-shadow: 0px 3px 5px 0px #686565;
        -moz-box-shadow: 0px 3px 5px 0px #686565;
        box-shadow: 0px 3px 5px 0px #686565;

        .title {
          color: #4682b4;
          font-size: 0.9rem;
          font-weight: 600;
          text-align: start;
          padding: 10px 20px;
        }

        .form-tag {
          width: 260px;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: flex-start;
          margin:0 20px 10px 20px;

          .label {
            font-size: 0.7rem;
            font-weight: 600;
            margin-bottom: 5px;
            .important {
              color: #ff0000;
              font-weight: bold;
            }
          }

          .input {
            width: 260px;
            height: 30px;
            border: 1px solid #ccc;
            padding: 5px 10px;
            transition: 0.4s;
          }
        }

        .btn {
          background: blueviolet;
          color: #fff;
          font-size: 0.8rem;
          text-transform: uppercase;
          text-decoration: none;
          padding: 5px 30px;
          border-radius: 5px;
          transition: linear 0.5s;
        }

        .btn:hover {
          background: lightskyblue;
        }
      }
    }
  }
}
</style>
