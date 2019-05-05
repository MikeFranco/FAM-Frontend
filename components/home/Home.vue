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
    <section class="form" >
      <transition name="fade" >
        <StudentForm v-if="show" class="form-student"/>
      </transition>
    </section>
  </div>
</template>

<script>
import StudentForm from '~/components/form-components/StudentForm.vue';

export default {
  components:{
    StudentForm
  },
  data(){
    return{
      show: false
    }
  },
  methods:{
    goToStudent(){
      //this.$router.push('/students')
      this.show = true;
    },
    goToEmployee(){
      this.$router.push('/employee')
    }
  }
}
</script>

<style scoped>
.form-student {
  position: absolute;
  top: 60%;
  left: 30%;

}
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

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}

</style>
