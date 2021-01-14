<template>
  <div>
    <div v-if="loading">
        <PageLoading/>
    </div>
    <transition>
      <div v-if="api" class="infos">
          <h1>Dúvidas ou Feedbacks?</h1>
          <br>
          <h2>{{api.titulo}}</h2>
          <p>{{api.descricao}}</p>
          <ul>
            <br>
            <li>
              <b>Email: </b>
              {{api.contato.email}}
            </li>
            <br>
            <li>
              <b>Telefone: </b>
              {{api.contato.telefone}}
            </li>
            <br>
            <li>
              <b>Endereço: </b>
              {{api.contato.endereco}}
            </li>
          </ul>

          <div class="contato">
            <img src="../assets/qai.png" alt="">
          </div>
          <hr>

          <div class="form">
            <h2>Formulário</h2>
            <!--formulário-->
            <form>
              <ul class="form-style-1">
                <li><label>Nome Completo   <span class="required">*</span></label><input type="text" name="field1" class="field-divided" placeholder="Nome" /> <input type="text" name="field2" class="field-divided" placeholder="Sobrenome" /></li>
                <li>
                    <label>Email  <span class="required">*</span></label>
                    <input type="email" name="field3" class="field-long" />
                </li>
                <li>
                    <label>Assunto </label>
                    <select name="field4" class="field-select">
                    <option value="Advertise">Problemas com pagamento</option>
                    <option value="Partnership">Não consigo acessar as aulas</option>
                    <option value="General Question">Outros</option>
                    </select>
                </li>
                <li>
                    <label>Deixe sua Mensagem <span class="required"></span></label>
                    <textarea name="field5" id="field5" class="field-long field-textarea"></textarea>
                </li>
                <li>
                    <input type="submit" value="Enviar" />
                </li>
              </ul>
            </form>
            <hr>
          </div>
          
          <div class="maisinformacoes">
            <h2>Para mais informações</h2>
            <h3>Acesse Nossas Redes Socias!</h3>
          </div>
          <div class="socialmidias">
            <a href="#" class="fa fa-facebook"></a>
            <a href="#" class="fa fa-twitter"></a>
            <a href="#" class="fa fa-linkedin"></a>
            <a href="#" class="fa fa-youtube"></a>
            <a href="#" class="fa fa-instagram"></a>
          </div>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData.js";

export default {
  name: "contato",
  mixins: [fetchData],
  
  created() {
    this.fetchData("/contato");
  }
}
</script>


<style scoped>

.infos h2 {
  margin-top: 21px;
}

.infos li {
  margin-top: 5px;
  font-size: 18px;
}

.contato img {
  align-content: center;
  margin-left: 50%;
  margin-top: -315px;
}

.maisinformacoes {
  text-align: center;
}

.maisinformacoes h2 {
  margin-top: 95px;
}

hr {
  width: 55px;
  background-color: #fefefe;
  margin-top: 55px;
}

.socialmedias {
  align-items: center;
  justify-content: center;
}

.fa {
  padding: 20px;
  font-size: 30px;
  width: 35px;
  text-align: center;
  text-decoration: none;
  margin: 5px 2px;
  margin-top: 45px;
  margin-left: 10%;
  border-radius: 50%;
}

.fa:hover {
    opacity: 0.7;
}

/* formulário */

.form-style-1 {
	max-width: 880px;
	padding: 20px 12px 10px 0px;
	font-family: 'Raleway', sans-serif;
}
.form-style-1 li {
  width: 100%;
	padding: 0;
	display: block;
	list-style: none;
	margin: 15px 0 0 -5px;
  
}
.form-style-1 label{
	margin:0 0 5px 5px;
	padding:0px;
	display:flex;
	font-weight: bold;
}
.form-style-1 input[type=text], 
.form-style-1 input[type=date],
.form-style-1 input[type=datetime],
.form-style-1 input[type=number],
.form-style-1 input[type=search],
.form-style-1 input[type=time],
.form-style-1 input[type=url],
.form-style-1 input[type=email],
textarea, 
select{
	box-sizing: border-box;
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	border:1px solid #BEBEBE;
	padding: 10px;
	margin:2px;
	-webkit-transition: all 0.30s ease-in-out;
	-moz-transition: all 0.30s ease-in-out;
	-ms-transition: all 0.30s ease-in-out;
	-o-transition: all 0.30s ease-in-out;
	outline: none;	
  font-family: 'Raleway', sans-serif;
}
.form-style-1 input[type=text]:focus, 
.form-style-1 input[type=date]:focus,
.form-style-1 input[type=datetime]:focus,
.form-style-1 input[type=number]:focus,
.form-style-1 input[type=search]:focus,
.form-style-1 input[type=time]:focus,
.form-style-1 input[type=url]:focus,
.form-style-1 input[type=email]:focus,
.form-style-1 textarea:focus, 
.form-style-1 select:focus{
	-moz-box-shadow: 0 0 8px #91b3fa;
	-webkit-box-shadow: 0 0 8px #91b3fa;
	box-shadow: 0 0 8px #91b3fa;
	border: 1px solid #91b3fa;
}
.form-style-1 .field-divided{
	width: 49%;
  border-radius: 5px;
}

.form-style-1 .field-long{
	width: 100%;
  border-radius: 5px;
}
.form-style-1 .field-select{
	width: 100%;
  border-radius: 5px;

}
.form-style-1 .field-textarea{
	height: 100px;
  border-radius: 5px;
}
.form-style-1 input[type=submit], .form-style-1 input[type=button]{
  height: 35px;
  width: 150px;
  cursor: pointer;
	background: #4648ef;
	padding: 8px 15px 8px 15px;
	border: none;
  border-radius: 5px;
	color: #fff;
}
.form-style-1 input[type=submit]:hover, .form-style-1 input[type=button]:hover{
	background: #19107c;
	box-shadow:none;
	-moz-box-shadow:none;
	-webkit-box-shadow:none;
}
.form-style-1 .required{
	color:red;
}


</style>
