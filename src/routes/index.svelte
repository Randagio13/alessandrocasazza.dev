<script>
	import Avatar from '../components/Avatar.svelte'
	import Intro from '../components/Intro.svelte'
	import Skills from '../components/Skills.svelte'
	import Footer from '../components/Footer.svelte'
	let logotypes = [
		{ src: 'html5.png', alt: 'HTML5', path: '//developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5', value: 95 },
		{ src: 'css3.svg', alt: 'CSS3', path: '//developer.mozilla.org/en-US/docs/Web/CSS', value: 95 },
		{ src: 'javascript.png', alt: 'Javascript', path: '//developer.mozilla.org/en-US/docs/Web/javascript', value: 95 },
		{ src: 'reactjs.svg', alt: 'ReactJS', path: '//reactjs.org', value: 95 },
		{ src: 'sveltejsLogo.png', alt: 'Svelte JS', path: '//sveltejs.dev', value: 75 },
		{ src: 'nextjs.svg', alt: 'Next JS', path: '//nextjs.org', value: 90 },
		{ src: 'gatsbyjs.png', alt: 'Gatsby JS', path: '//gatsbyjs.org', value: 90 },
		{ src: 'php.svg', alt: 'Php', path: '//php.net', value: 85 },
		{ src: 'python.png', alt: 'Python', path: '//www.python.org', value: 65 },
		{ src: 'nodejs.png', alt: 'Node JS', path: '//nodejs.org', value: 80 },
		{ src: 'mysql.png', alt: 'Mysql', path: '//mysql.com', value: 85 },
		{ src: 'postgresql.png', alt: 'Postgresql', path: '//www.postgresql.org', value: 75 },
	]
	let socialIcons = [
		{ src: 'github.svg', alt: 'Github', path: '//github.com/Randagio13' },
		{ src: 'twitter.svg', alt: 'Twitter', path: '//twitter.com/randagio19' },
		{ src: 'linkedin.svg', alt: 'Linkedin', path: '//www.linkedin.com/in/alessandrocasazza/' },
	]
</script>
<script context="module">
  export function preload({ params, query }) {
    return this.fetch("sitemap.xml");
  }
</script>
<svelte:head>
	<title>Alessandro Casazza - Senior Frontend Developer</title>
</svelte:head>

<div class="bg-red-600 px-10 py-16 shadow-md">
	<div class="container mx-auto flex flex-wrap md:flex-no-wrap justify-center items-center content-center block text-center md:text-left">
		<div class="w-1/2 flex justify-end">
			<Avatar className="mx-auto h-40 w-40 rounded-full md:mr-6 object-cover shadow-md" src="ale.jpg" alt="Alessandro Casazza" />
		</div>
		<Intro className="w-full md:w-3/4 leading-relaxed" />
	</div>
</div>
<div class="mx-auto bg-gray-200 p-10 shadow-inner">
	<div class="container mx-auto">
		<h2 class="text-center">Skills</h2>
		<Skills {logotypes} />
	</div>
</div>
<Footer {socialIcons} />