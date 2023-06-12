<script>
export default {
	data: function() {
		return {
			errormsg: null,
			loading: false,
			some_data: ""
		}
	},
	methods: {
        data(){
        },
	},
	async mounted(){
		try{
            let response = await this.$axios.get(`/`);
        } catch(e){
            this.errormsg = e.message
        }
	}
}
</script>

<template>
	<div class="TitlePageHome">
			Micro Algae Database
	</div>
	<div v-if="errormsg">
		Error:
		<ErrorMsg :msg="errormsg"></ErrorMsg>
	</div>
	<div class="bodyHome">
		<div class="sectionHome">
			First Micro Algae Platform
		</div>
		<div class="contentHome">
			<span class="span-bold">Vulgaris MicroAlgae</span> is the world's first platform of microalgae with carbon capture properties. 
			MicroAlgae is a database for consulting taxonomic, nucleotide and protein data on over 900+ species of microalgae.
			<div class="imagesHome">
				<img src="/images/Chlorella_img.jpg" alt="Chlorella" title="Chlorella">
				<img src="/images/Scenedesmus_img.jpg" alt="Scenedesmus" title="Scenedesmus">
			</div>
			<div style="display:flex;">
				<figcaption>Chlorella Vulgaris</figcaption>
				<figcaption class="right-fig">Scenedesmus Obliquus</figcaption>
			</div>

		</div>
		<div class="sectionHome">
			Current in Vulgaris Platform
		</div>
		<div class="contentHome">
			<span class="span-underline">969</span> species, <span class="span-underline">510.440</span> nucleotide and <span class="span-underline">612.654</span> protein entries, <span class="span-underline">21</span> genomes data and <span class="span-underline">12</span> species with <span class="span-underline">30</span> bioprojects.
		</div>
	</div>
</template>

<style>
.TitlePageHome {
    font-size: 48px;
	margin-left: 25%;
    color: orange;
}
.TitlePageHome:hover, .TitlePageHome:focus, .TitlePageHome:active { 
    /* color:#ffcc00;  */
    text-shadow: 0 4px 6px #000; 
}
.bodyHome{
	margin-top: 5%;
}
.sectionHome {
	margin-top: 3%;
	font-size: 28px;
	color:#757575;
}
.sectionHome:hover, .sectionHome:focus, .sectionHome:active { 
    /* color:#ffcc00;  */
    text-shadow: 0 4px 6px #000; 
}
.contentHome{
	margin-left: 3%;
	margin-right: 3%;
	margin-top: 2%;
	font-size: 16px;
	word-wrap:break-word;
}
.contentHome:hover {
	text-shadow: 0 6px 8px #000; 
}
.imagesHome{
	margin-top: 2%;
	gap: 10%;
	display:flex;
}
.imagesHome img{
	width: 400px;
	height: 400px;
}

.right-fig{
	margin-left: 364px;
}

.span-underline {
  text-decoration: underline;
}

.span-bold {
	font-weight: bold;
}
</style>