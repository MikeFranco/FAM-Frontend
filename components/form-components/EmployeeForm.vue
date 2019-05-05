<template>
  <section>
    <body>
    <div class="banner">
      <video autoplay muted loop src="./b.mp4"></video>
      <div class="content">
      <div class="con-img" > <img src="~/assets/logos/fam.jpeg" class="imagen"> </div>
        <h1>Form</h1>
        <form class="" action="index.html" method="post">

          <label for="">Name</label>
          <input placeholder="Name" type="text" name="" value="">

          <label for="">Last Name</label>
          <input placeholder="Last Name" type="text" name="" value="">

          <label for="">Ocuppation</label>
          <input placeholder="Occupation" type="text" name="" value="">

          <label for="">Entry</label>
          <input placeholder="Entry" type="text" name="" value="">

        </form>
      </div>
  </div>
  </body>
  </section>
</template>

<script>
export default {

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

</style>
