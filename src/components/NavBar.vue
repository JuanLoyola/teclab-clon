<template>
  <div id="nav">
      <div class="nav--logo">
        <a href="#"><img class="logo" src="@/assets/logo.png" alt="logo"></a>
      </div>
      <div>
        <input type="checkbox" id="click">
      <label for="click" class="menu-btn">
        <i class="fas fa-bars"></i>
      </label>
      <ul class="menu">
        <li><a href="#">Carreras</a></li>
        <li><a href="#">¿Quienes somos?</a></li>
        <li><a href="#">Aspirante</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contacto</a></li>
        <li><a href="#">Alumno</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style lang="scss">
#nav {
  width: 100%;
  height: 70px;
  padding-top: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  z-index:3;

    .logo {
    margin-left: 100px;
    width: 130px;
  }

  .menu{
    margin-right: 100px;
  }
}
#nav ul{
    display: flex;
    flex-wrap: wrap;
    list-style: none;
  }
  #nav ul li{
    margin: 0 2px;
  }
  #nav ul li a{
    color: #fff;
    text-decoration: none;
    font-size: 0.8rem;
    font-weight: 700;
    text-transform: uppercase;
    text-shadow: 1px 1px 1px #333;
    padding: 8px 0.6rem;
    letter-spacing: 1px;
    transition: all 0.3s linear;
  }
  #nav ul li a:hover {
    color: #a5d422;
    border-bottom: 1px solid #7b5da5;
  }

  #nav .menu-btn i{
    color: #fff;
    font-size: 22px;
    padding: 0 30px;
    cursor: pointer;
    display: none;
  }

  input[type="checkbox"] {
    display: none;
  }
  @media (max-width: 1000px){
    #nav{
      height: 55px;
      padding: 0 40px 0 50px;
      background: rgba(0, 0, 0, 0.9) ;
      justify-content: space-between;
    }
  }
  @media (max-width: 920px) {
    #nav .menu-btn i{
      display: block;
    }
    #click:checked ~ .menu-btn i:before{
      content: "\f00d";
    }
    #nav ul{
      position: fixed;
      top: 55px;
      left: -100%;
      background: #222121;
      height: 100vh;
      width: 100%;
      text-align: center;
      display: block;
      transition: all 0.3s ease;
    }
    #click:checked ~ ul{
      left: 0;
    }
    #nav ul li{
      width: 100%;
      margin: 40px 0;
    }
    #nav ul li a{
      width: 100%;
      margin-left: -100%;
      display: block;
      font-size: 20px;
      transition: 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
    #click:checked ~ ul li a{
      margin-left: 0px;
    }
    #nav ul li a.active,
    #nav ul li a:hover{
      background: none;
      color: #F27373;
    }
  }
  @media screen and (min-width: 320px) and (max-width:1034px){
    #nav{
      padding: 0px 0px;
      display:flex;
      width:100%;

      .name{
        font-size: 0.8rem;
      }

      a{
        font-size: 0.6rem;
        display:flex;
        flex-direction: row wrap;
      }
    }
  }
</style>
