<script lang="ts">
	import Infobox from '$lib/components/Infobox.svelte';
	import Section from '$lib/components/Section.svelte';
	import TableOfContents from '$lib/components/TableOfContents.svelte';

	const pageTitle = 'Oliver Boorstein';

	const infoboxItems = [
		{ label: 'Born', value: '2004-09-25' },
		{ label: 'Occupation', value: 'Student' },
		{ label: 'University', value: 'University of Oregon' },
		{ label: 'Major', value: 'Computer Science' },
		{ label: 'GPA', value: '4.25' },
		{ label: 'Email', value: 'obo@uoregon.edu' },
		{ label: 'Website', value: 'oliboo.wiki' },
		{ label: 'LinkedIn', value: 'linkedin.com/in/oliboo' },
		{ label: 'GitHub', value: 'github.com/flamboh' }
	];

	// Define sections for the Table of Contents
	const sections = [
		{ title: 'About Me', id: 'about-me' },
		{ title: 'Technical Skills', id: 'technical-skills' },
		// { title: 'Experience', id: 'experience' },
		{ title: 'Projects', id: 'projects' }
		// { title: 'Contact', id: 'contact' }
	];
</script>

<svelte:head>
	<title>{pageTitle}</title>
</svelte:head>

<h1 class="mb-6 border-b border-gray-300 pb-4 text-4xl font-bold">{pageTitle}</h1>

<Infobox title={pageTitle} items={infoboxItems}></Infobox>

<TableOfContents {sections} />

<Section title="About Me" id="about-me">
	<p>
		Oliver Boorstein is a computer science student at the University of Oregon. They are currently
		working on research with the Oregon Network Research Group.
	</p>
</Section>

<Section title="Technical Skills" id="technical-skills">
	<ul class="mt-2 ml-6 list-disc">
		<li>Python</li>
		<li>JavaScript / TypeScript</li>
		<li>C</li>
		<li>C++</li>
		<li>Svelte / SvelteKit</li>
		<li>React</li>
		<li>Tailwind CSS</li>
		<li>HTML / CSS</li>
		<li>Git</li>
	</ul>
</Section>

<!-- <Section title="Experience" id="experience">
	<p></p>
</Section> -->

<Section title="Projects" id="projects">
	<div class="mt-4">
		<h3 class="text-xl font-semibold">Pedagoggles | LA Hacks 2025</h3>
		<p class="text-sm text-gray-600">
			Tech stack: Spectacles, Lens Studio, Gemini, TypeScript, React
		</p>
		<p class="mt-1">
			A team project for LA Hacks 2025. We collaborated to create an augmented reality Lens for Snap
			Inc.'s experimental AR device Spectacles that enhances the classroom experience.
		</p>
		<a
			href="https://github.com/danila6231/Pedagoggles-AR"
			class="text-blue-600 hover:underline"
			target="_blank"
			rel="noopener noreferrer">GitHub Repo</a
		>
	</div>
	<div class="mt-4">
		<h3 class="text-xl font-semibold">The Stoning</h3>
		<p class="text-sm text-gray-600">
			Tech stack: React, TypeScript, Tailwind CSS, Cloudflare Pages
		</p>
		<p class="mt-1">
			A music publication website that hosts articles and reviews from writers on The Stoning team.
			Developed as a group stemming from a student organization at the University of Oregon.
		</p>
		<a
			href="https://www.thestoning.net/"
			class="text-blue-600 hover:underline"
			target="_blank"
			rel="noopener noreferrer">Live Site</a
		>
	</div>
</Section>
<!-- 
<Section title="Contact" id="contact">
	<p>
		Provide ways for people to contact you, such as email or links to your LinkedIn, GitHub, or
		other professional profiles.
	</p>
</Section> -->
