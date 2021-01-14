<template>
  <div>
    <div v-if="loading">
        <PageLoading/>
    </div>
    <transition>
      <div v-if="api" class="conteudo">
        <div>
          <h1>{{api.titulo}}</h1>
          <p>{{api.descricao}}</p>
          <img src="../assets/aula.png" alt="">
        </div>
          <ul class="cursos-lista">
            <li v-for="curso in api.cursos" :key="curso.id">
              <h2>
                <router-link :to="{name: 'curso', params: {curso: curso.id}}">
                {{curso.nome}} - {{curso.totalAulas}} aulas | {{curso.horas}} horas
                </router-link>
              </h2>
              <p>{{curso.descricao}}</p>
            </li>
            <hr>
          </ul>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";



export default {
  name: "cursos",
  mixins: [fetchData],

  created(){
      this.fetchData("/cursos");
  }
}
</script>

<style scoped>

hr {
  width: 55px;
  background-color: #fefefe;
  margin-top: 55px;
}
img {
  width: 95%;
  margin-top: 30px;
}

.cursos-lista {
  margin-top: 55px;
}

.cursos-lista li{
  margin-bottom: 50px;
}

</style>
