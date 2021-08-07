<template>

	<div class="main">
		<div class="div1">
			<custom-banner-vue></custom-banner-vue>
			<div class="subdiv1">		
				<custom-banner-vue :options="options2"></custom-banner-vue>		
			</div>
		</div>
		<div class="div2">
			<custom-banner-vue :options="options"></custom-banner-vue>
		</div>
	</div>

</template>

<script>
import { CustomBannerVue } from 'custom-banner-vue';

export default{
	name:'Demobanner',
	components:{
		CustomBannerVue
	},
	data(){
		return {
			//banner vertical
			options:{
				time:10000,
				orientation:"vertical",
				images:[
					[

					],
					[
						"img/pizza-maker.jpg",
						"img/datafono3.jpg",
						
					],
					[
						"img/pizza.jpg",
						"img/hamburguesa.jpg",
						"img/lasaña.jpg"

					]
				],
				texts:[
					[						
						"Horno de piedra",
						"Servicio a domicilio",
						"Pago con tarjeta",

					],
					[],
					[]
				],
				effects:{
					1:{
						modeText:true,
						fontSizeStyle:"30px"
					},
					2:{
						left:true
					},
					3:{

					}
				},
				order:{
					0:[3],
					1:[1,3],
					2:[1,2],
					3:[3],
					4:[1,2]
				}
			},
			//banner pequeño 
			options2:{
				orientation:"horizontal",
				size:"min",				
				images:[
					[
						
					],
					[
						"img/singapore.jpg",
						"img/crucero2.jpg",
						"img/venecia.jpg"
					],
					[
						
					]
				],
				texts:[
					[
						"Disfruta de los mejores hoteles,",
						"vuelos, cruceros y mucho más",
						"a un precio inmejorable"
						//"convierte tus vacaciones",						
						//"en una experiencia inolvidable"
					],
					[
						
						
						
					],
					[						
						"RESERVA YA",
						"con descuentos de HASTA EL 50%",
						"Llama ya al 656 56 56 56",
						"...o entra en www.tuviaje.es"
						
					]
				],
				effects:{
					1:{
						fontSizeStyle:"19px",
						modeText:true,
						left:true
					},
					2:{
						opacity:true,
						height:true,
						
					},
					3:{
						fontSizeStyle:"19px",
						modeText:true,
						rotate:true
					}
				},
				order:{
					0:[1,3],
					1:[2],
					2:[1,3],
					3:[2]
				}

			}
		}
	}
}

</script>
<style>
*{
	font-family: Quicksand;
	font-weight: bold;
}
.div1{
	display:inline-block;
}
.subdiv1{
	margin-top:50px;
	
}
.subdiv1 p{
	color: white !important;
}
.subdiv1 .text1{
	color: #ffff00 !important;

}
.div2{
	float: left;

}
@media (max-width: 1050px){
	.div2{		
		float: none;
		margin: auto;
		width: 100%;
		display: block;
	}	
}
@media (max-width: 850px){
	.main{
		display:inline-block
	}
}

</style>