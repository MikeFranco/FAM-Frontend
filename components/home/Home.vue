<template>
  <div>
    <div class="logo">
      <img src="~/assets/logos/fam.jpeg">
    </div>
    <section class="container" @click="goToStudent" >
        <section class="card">
          <div>
            <h1 > Estudiante </h1>
          </div>
        </section>
    </section>
    <section class="container2" @click="goToEmployee">
      <section class="card">
        <div> <h1 align="center"> Profesores </h1> </div>
      </section>
    </section>
  </div>
</template>

<script>

export default {
  methods:{
    goToStudent(){
      this.$router.push('/students')
    },
    goToEmployee(){
      this.$router.push('/employee')
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
  flex-direction: column;
  justify-content: center;
  border-radius: 50px;
}

.container2 {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 15%;
  height: 7%;
  position: absolute;
  top: 40%;
  left: 60%;
  display: flex;
  text-align: center;
  flex-direction: column;
  justify-content: center;
  border-radius: 50px;
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

.logo{
  position: absolute;
  top: 0%;
  left: 37%;
}
</style>
