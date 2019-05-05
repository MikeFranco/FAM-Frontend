<template>
  <section>
    <transition name="slide-fade">
      <div v-if="showForm" class="container" >
        <div class="row">
          <div class="column">
            <div class="card">Viajes</div>
          </div>
          <div class="column">
            <div class="card">Compras</div>
          </div>
          <div class="column">
            <div class="card">Educación</div>
          </div>
          <div class="column">
            <div class="card">Personal</div>
          </div>
        </div>
      </div>
    </transition>
  </section>
</template>

<script>
export default {
  data(){
    return{
      showForm: false
    }
  },
  mounted(){
    this.showForm = true;
  }
}
</script>

<style scoped >

.slide-fade-enter-active {
  transition: all .3s ease;
}

.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}

.slide-fade-enter, .slide-fade-leave-to{
  transform: translateX(10px);
  opacity: 0;
}

* {
  box-sizing: border-box;
}

body {
  font-family: Arial, Helvetica, sans-serif;
}

.column {
  float: left;
  width: 25%;
  padding: 0 10px;
}

.row {margin: 0 -5px;}

.row:after {
  content: "";
  display: table;
  clear: both;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* this adds the "card" effect */
  padding: 16px;
  text-align: center;
  background-color: #f1f1f1;
}

@media screen and (max-width: 600px) {
  .column {
    width: 100%;
    display: block;
    margin-bottom: 20px;
  }
}

.container {
  transition: 0.3s;
  position: absolute;
  top: 40%;
  left: 10%;
  display: flex;
  text-align: center;
  flex-direction: column;
  justify-content: center;
  border-radius: 50px;
}

</style>
