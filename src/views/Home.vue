<template>
  <div>
    <div v-if="loading">
      <PageLoading/>
    </div>
    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1>Sobre a {{api.titulo}}</h1>
          <p>{{api.descricao}}</p>
          <hr>
          <router-link class="btn-cursos" tag="button" to="/cursos">Cursos</router-link>
          <div>
            <br>
            <div>
              <h2>Diferenciais</h2>
              <p>Tecnologias que estão sendo utilizada no mercado de trabalho.</p>
              <hr>
              <div class="game-board">
                <div class="box"><img src="../assets/tech-icons/030-html-5.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/031-css.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/029-javascript.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/026-sass.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/006-react.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/032-nodejs.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/021-mysql.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/027-php.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/025-typescript.png" alt=""></div>
                <div class="box"><img src="../assets/tech-icons/015-ruby.png" alt=""></div>
              </div>
            </div>
            <div d-planos>
              <h2>Exclusividades para Alunos</h2>
              <br>
              <p>Hackathons, Webinars e muito mais...</p>
            </div>
          </div>
          <hr>
        </div>
        <img src="../assets/home-pic-pc.png" alt="imagem tech - aprender">
        <div id="sec-2-img">
          <img src="../assets/hckthon.jpg" alt="">
        </div>
        <div id="sec-2-content">
          <img src="../assets/webinar.png" alt="">
        </div>
        <h2 id="depoimentos">Depoimentos</h2>
      </div> 
    </transition>
    <div class="avaliacoes">
      <ul>
        <li v-for="avaliacao in api.avaliacoes" :key="avaliacao.nome">
        <p>{{avaliacao.nome}}</p>
        <div class="nome-avaliacao">
        <p>"{{avaliacao.descricao}}"</p>
        </div>
        </li>
        </ul>        
    </div>
  </div>
  
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "home",
  mixins: [fetchData],
  
  created() {
    this.fetchData("/home");
  }
};

</script>

<style scoped>

.nome-avaliacao {
  background-color: #1a1b63;
  color: white;
  width: 100%;
  height: 35;
  padding: 1px;
  border-radius: 5px;
  box-shadow: 0 4px 2px rgba(0, 0, 0, 0.1);
}

.nome-avaliacao p {
  font-size: 15px;
  font-style: italic;
  margin-left: 15px;
}

.avaliacoes ul, li{
  border-radius: 15px;
  padding: 3px;
}

.conteudo img {
  width: 100%;
  margin-top: 50px;
}

.btn-cursos {
  width: 325px;
  border: none;
  background:#4648ef;
  border-radius: 4px;
  color: white;
  cursor: pointer;
  padding: 15px 20px;
  font-size: 1rem;
  margin-top: 10px;
  margin-bottom: 40px;
  box-shadow: 0 4px 2px rgba(0, 0, 0, 0.1);
  font-family: 'Raleway', sans-serif;
}

.btn-cursos {
  transition-duration: 0.4s;
}

.btn-cursos:hover {
  background-color:#19107c;
  color: white;
}

.game-board {
    margin-left: -15px;
    display: grid;
    grid-template-rows: 95px 95px 95px;
    grid-template-columns: 95px 95px 95px 95px 95px;
}

body {
  display: flex;
  justify-content: center;

}

hr {
  width: 35px;
  margin-left: 0;
}

#depoimentos {
  margin-top: 50px;
}

.box {
  padding: 25px;
  display: flex;
  align-items: center;
  justify-content: center;
}

#sec-2-img {
  flex: 1;
}

#sec-2-content {
  flex: 2;
}
#sec-2-img img {
  height: 275px;
  width: 455px;
  box-shadow: 1px 1px 5px  grey;
}
#sec-2-content img{
  height: 275px;
  width: 435px;
  box-shadow: 1px 1px 5px  grey;
}

</style>
