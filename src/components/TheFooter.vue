<template>
    <footer class="footer-distributed">
        
			<div class="footer-left">

				<h3>Escola de Tecnologia</h3>
                <br>
				<p class="footer-company-name">Todos os direitos reservados © 2020</p>
			</div>

			<div class="footer-center">

				<div>
					<i class="fa fa-map-marker"></i>
					<p><span>Botafogo, Rj</span>Rua Ali Perto</p>
				</div>

				<div>
					<i class="fa fa-phone"></i>
					<p>+55 (21) 9999-9999</p>
				</div>

				<div>
					<i class="fa fa-envelope"></i>
					<p><a href="#">suporte@escoladetecnologia.com</a></p>
				</div>

			</div>

			<div class="footer-right">

				<p class="footer-company-about">
					<span>Sobre</span>
					Escola de programação 100% online que forma profissionais capacitados para o mercado de trabalho, abordando
                    todas as tecnologias utilizadas pelas grandes empresas. Através de um método de ensino que garante o aprendizado
                    de maneira mais prática.
				</p>

				<div class="footer-icons">

					<a href="#"><i class="fa fa-facebook"></i></a>
					<a href="#"><i class="fa fa-twitter"></i></a>
					<a href="#"><i class="fa fa-linkedin"></i></a>
					<a href="#"><i class="fa fa-github"></i></a>

				</div>

			</div>

		</footer>
</template>

<script>
export default {
    name: "TheFooter"
    
};
</script>

<style>

footer {
    background: #4648ef;
    padding: 25px 0;
    text-align: center;
    font-size: 1.2rem;
    color: #fff;
    position: relative;
    top: 350px;
}

.footer-distributed{
	background:rgb(247,249,255);
	box-shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.12);
	box-sizing: border-box;
	width: 100%;
	text-align: left;
	font: bold 16px sans-serif;
	padding: 55px 50px;
}

.footer-distributed .footer-left,
.footer-distributed .footer-center,
.footer-distributed .footer-right{
	display: inline-block;
	vertical-align: top;
}

.footer-distributed .footer-left{
	width: 40%;
}

.footer-distributed h3{
	color:  #19107c;
	font-family: 'Raleway', sans-serif;
    font-size: 2.5rem;
	margin: 0;
}

.footer-distributed .footer-company-name{
	color: #19107c;
	font-size: 15px;
	font-weight: lighter;
	margin: 0;
}

.footer-distributed .footer-center{
	width: 35%;
}

.footer-distributed .footer-center i{
	background-color: #4648ef;
	color: #ffffff;
	font-size: 25px;
	width: 38px;
	height: 38px;
	border-radius: 50%;
	text-align: center;
	line-height: 42px;
	margin: 10px 15px;
	vertical-align: middle;
}

.footer-distributed .footer-center i.fa-envelope{
	font-size: 17px;
	line-height: 38px;
}

.footer-distributed .footer-center p{
	display: inline-block;
	color: #19107c;
    font-weight:400;
	vertical-align: middle;
	margin:0;
}

.footer-distributed .footer-center p span{
	display:block;
	font-weight: normal;
	font-size:14px;
	line-height:2;
}

.footer-distributed .footer-center p a{
	color: #19107c;
	text-decoration: none;;
}


.footer-distributed .footer-right{
	width: 20%;
}

.footer-distributed .footer-company-about{
	line-height: 20px;
	color: #19107c;
	font-size: 13px;
	font-weight: normal;
	margin: 0;
}

.footer-distributed .footer-company-about span{
	display: block;
	color:  #19107c;
	font-size: 15px;
	font-weight: bold;
	margin-bottom: 20px;
}

.footer-distributed .footer-icons{
	margin-top: 25px;
}

.footer-distributed .footer-icons a{
	display: inline-block;
	width: 35px;
	height: 35px;
	cursor: pointer;
	background-color: #4648ef;
	border-radius: 2px;
	font-size: 20px;
	color: #ffffff;
	text-align: center;
	line-height: 35px;
	margin-right: 3px;
	margin-bottom: 5px;
}

@media (max-width: 880px) {

	.footer-distributed{
		font: bold 14px sans-serif;
	}

	.footer-distributed .footer-left,
	.footer-distributed .footer-center,
	.footer-distributed .footer-right{
		display: block;
		width: 100%;
		margin-bottom: 40px;
		text-align: center;
	}
    
	.footer-distributed .footer-center i{
		margin-left: 0;
	}
}

</style>