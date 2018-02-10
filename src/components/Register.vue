<template>
  <div class="home">
    <p class="nome"> REGISTER </p> 
    <div class="box"> 
      <form @submit.prevent="sendEmail">
        <label>Nome:</label>
        <input type="text" name="Nome" v-model="name" value="Seu Nome Aui" required="required">
      <br><br>
        <label>Email:</label>
        <input type="email" name="Email" v-model="email" value="Seu Eamil Aqui" required="required">
      <br><br>
      <label>Senha:</label>
        <input type="senha" name="senha" v-model="senha" value="Sua Senha Aqui" required="required">
      <br><br>
        <button>ENVIAR</button>
        </form>
      </div>
      </div>
</template>

<style>
  @import url('https://fonts.googleapis.com/css?family=Anton');
  @import url('https://fonts.googleapis.com/css?family=Encode+Sans+Expanded');
 
  .imagemHome {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: -1;
    height: 100%;
  }
   .nome  {
    color: rgba(244, 206, 66, 0.9);
    font-size: 80px;
    font-family: Anton;
    right: 110px;
    bottom: 300px;
    position: absolute;
   /* text-shadow: #000000 1px 2px 2px;*/

  }
</style>