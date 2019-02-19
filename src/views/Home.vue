<template>
	<div class="container">
		<div class="nav">
			<a href="#">Home</a>
			<a href="#projects">Projects</a>
			<a href="#contact">Contact</a>
			<a href="https://drive.google.com/file/d/1qNbRcSgR82zhEJjFwfruKMLoxne-qrUY/view?usp=sharing">Resume</a>
		</div>

		<div class="hero-logo">
			Ioana_Moraru<span class="cursor-main-color">&nbsp</span>
		</div>

		<div class="hero-description">
			I am a tech girl who is passionate about coding and algorithms. I am a hard-working person and I always want to get thing done in time. I am eager to learn new programming languages and concepts, so I am looking for a challenging development position.
		</div>

		<terminal></terminal>
		
		<div id="projects" class="section">Projects</div>

		<Project title="Programare cu rabdare" 
				 :showReadMore="false"
				 :technologies="['Java', 'Teaching', 'Interview']" >
				 
			<img :src="getBannerPath('programare.jpg')">

			<p>
				Pe 16 februarie 2019 am participat la cercul de informatica <a href="http://programarecurabdare.ro/">Programare cu rabdare</a> din Bacau unde le-am vorbit participantilor despre experienta mea la Google si am rezolvat impreuna probleme de interviu.
			</p>

			<p> 
				Puteti gasi rezolvarea problemelor <a href="https://github.com/ioanam14/interview_questions.git">aici</a> si prezentarea <a href="https://drive.google.com/open?id=1B8nym90tVxXE1COirkoYHq8q30F5SyXV">aici</a>.
			</p>

		</Project>

		<Project title="Google Internship" 
				 :showReadMore="true" 
				 readMoreLink="https://codette.ro/blog/step-internship-software-engineer-google-london/">
				 
			<img :src="getBannerPath('internship.jpg')">

			<p>
				Bună, sunt Ioana și în prezent sunt studentă în anul 3 la Facultatea de Automatică și Calculatoare în București. Vara aceasta am avut parte de o experiență cu totul nouă pentru mine care s-a dovedit a fi foarte interesantă: am fost STEP (Summer Trainee Engineering Program) Intern Software Engineer la Google în Londra. 
			</p>

			<p>
				Acest timp de internship este destinat studenților care termină anul 1 din 3 ani de licență sau anul 2 din 4 ani. Prin urmare, acesta este un program bazat mai mult pe învățare pentru persoane care nu au prea multă experiență în acest domeniu. Față de un internship normal, acesta se deosebește prin faptul că se lucrează în perechi și proiectele sunt mai puțin dificile. Pentru mine acest internship a fost prima oară când am lucrat în industrie și pot spune că a fost un început excelent pentru viitoarea mea carieră în domeniul IT&C.
			</p>
		</Project>

		<Project title="Online blog" 
				 :showReadMore="false" 
				 :technologies="['PHP', 'Laravel', 'MySQL']">
				 
			<img :src="getBannerPath('blog.jpg')">

			<p>
				This is a website where a user can create an account, make a post, see others' posts and comment on posts. You can find the 
				repo <a href="https://github.com/ioanam14/blog">here</a>.
			</p>
		</Project>

		<div id="contact" class="section">Contact</div>

		<div class="contact">
			<div class="email">ioanamoraru14@gmail.com</div>
			<div class="links">
				<a href="https://github.com/ioanam14">Github</a>
				<a href="https://instagram.com/ioanamoraru14">Instagram</a>
				<a href="https://linkedin.com/in/ioana-moraru-789b59122">LinkedIn</a>
				<a href="https://facebook.com/ioana.moraru.14">Facebook</a>
			</div>
		</div>	
	</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Terminal from "@/components/Terminal.vue";
import Project from "@/components/Project.vue";

@Component({
	components: {
		Terminal,
		Project,
	},
	methods: {
		getBannerPath (filename) {
			return filename ? require(`../assets/img/${filename}`) : ''
		}
	},
})
export default class Home extends Vue {}
</script>
