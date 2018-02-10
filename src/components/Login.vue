<template>
<!-- A rota do login e do register precisa ser digitada porque de algum modo ta puxando
do projeto antigo, ai fica about e services e a tela fica em branco -->

  <div class="about">
  <div class="textoAb">
      <p> LOGIN</p> 
  </div>
  <div class="box"> 
      <form @submit.prevent="sendEmail">
        <label>Nome:</label>
        <input type="text" name="Nome" v-model="name" value="Seu Nome Aui" required="required">
      <br><br>
        <label>Email:</label>
        <input type="email" name="Email" v-model="email" value="Seu Eamil Aqui" required="required">
      <br><br>
        <button>ENVIAR</button>
        </form>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data(){
    return {
      title:'Login',
    };
  },
  methods: {
    getAboutInfo(){
      axios.get('localhost:1207/login')
      .then((res) => {
        console.log(res);
      }).catch((err) => { console.log(err); });
    },
  },
  beforeCreate(){
    this.getAboutInfo();
  },
};
</script>
<style>
  @import url('https://fonts.googleapis.com/css?family=Anton');
  @import url('https://fonts.googleapis.com/css?family=Shadows+Into+Light');
  @import url('https://fonts.googleapis.com/css?family=Encode+Sans+Expanded|Shadows+Into+Light');

  .box {
    position: absolute;
    margin-left: 300px;
    margin-bottom: 10px;

  }
  .imagemAbout {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: -1;
    height: 100%;
  }
  .textoAb  {
    color: rgba(244, 206, 66, 0.85);
    font-size: 80px;
    font-family: Anton;
    right: 110px;
    bottom: 300px;
    position: absolute;
   /* text-shadow: #000000 1px 2px 2px;*/

  }

  .descricao {
    color: white;
    position: absolute;
    font-size: 18px;
    font-family: Encode Sans Expanded|Shadows Into Light;
    box-shadow: #000 2px 2px 1px;
    bottom: 55px;
    left: 160px;
    border: #000 1px solid;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.3);
  }
  .cabecalho {
    color: white;
    position: absolute;
    font-size: 50px;
    font-family: Shadows Into Light;
    bottom: 120px;
    left: 430px;
    text-shadow: #000000 1px 2px 2px;
  }

</style>