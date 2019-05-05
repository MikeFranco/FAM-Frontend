<template>
  <div>
    <div>
      <h1>FAM</h1>
    </div>
    <section class="container" >
        <section class="card">
          <div @click="goToStudent">
            <h1 > Estudiante </h1>
          </div>
        </section>
    </section>
    <section class="container2">
      <section class="card">
        <div> <h1 @click="goToStudent"> Profesores </h1> </div>
      </section>
    </section>
  </div>
</template>

<script>

export default {
  methods:{
    goToStudent(){
      this.$noty.error('¡Ups! Parece que hubo un error')
    }
  }
}
</script>

<style scoped>

.container {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 15%;
  position: absolute;
  top: 40%;
  left: 25%;
  display: flex;
  text-align: center;
}

.container2 {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 15%;
  height: 8%;
  position: absolute;
  top: 40%;
  left: 60%;
  display: flex;
  text-align: center;
}

.container:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container2:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.card {
  padding: 2px 16px;
  text-align: center;
}
</style>
