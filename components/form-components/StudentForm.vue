<template>
  <section>
    <body>
    <div class="banner">
      <video autoplay muted loop src="./b.mp4"></video>
      <div class="content">
      <div class="con-img" > <img src="~/assets/logos/fam.jpeg" class="imagen"> </div>
        <h1>Inicio de sesión</h1>
        <form class="" action="index.html" method="post">

          <label for="">Nombre(s)</label>
          <input placeholder="Nombre(s)" type="text">

          <label for="">Apellidos</label>
          <input placeholder="Apellidos" type="text">

          <label for="">¿Eres foráneo?</label>
          <select
            class="form-control custom-select fix-select-styles"
            v-model="foraneo"
            style="border: 1px solid black;">
            <option disabled value="">Seleccione una opción</option>
            <option>Si</option>
            <option>No</option>
            </select>

          <label for="">¿Trabajas?</label>
          <select
            class="form-control custom-select fix-select-styles"
            v-model="employee"
            style="border: 1px solid black;">
            <option disabled value="">Seleccione una opción</option>
            <option>Si</option>
            <option>No</option>
          </select>

        </form>
      </div>
  </div>
  </body>
  </section>
</template>

<script>
export default {
  data(){
    return{
      foraneo: 'Selecciona una opción',
      employee: 'Selecciona una opción',
    }
  }
}
</script>

<style>

body{
  padding: 0;
  margin:0 ;
  font-family: 'Poppins', sans-serif;
}
.banner{
  width: 100%;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;

}
.banner video{
  position: absolute;
  top:0;
  left: 0;
  object-fit: cover;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.banner .content{
  position: relative;
  z-index: 1;
  text-align: center;
}

.content{
  margin: 1em;
  width: 24%;
  height: 40%;
  border: double #070707;
  border-radius: 30px;
  background-color:rgba(239,239,239,0.4);
  box-shadow: 6px 4px 8px rgba(0, 0, 0, 0.3);
}

label{
  display: block;
}

.imagen{
  width: 150px;
  height: 150px;
  border-radius: 25px;
}

.con-img{
  padding-top: 10px;
  padding-bottom: 10px;
}

.form-control {
  height: 50px;
  border-color: black;
  border-radius: 15px;
}



</style>
