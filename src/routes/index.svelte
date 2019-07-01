<script>
	const projects = [
		{
			name: 'Fiber Finder',
			link: 'https://github.com/bytesizedpcs/FiberFinder',
			description: `a web app created in Node.js and React to view aparments with Google Fiber in your area.`,
		},
		{
			name: 'Coinview',
			link: 'https://github.com/bytesizedpcs/Coinview',
			description: `a web app created in Vue and Node.js to aid in the filtration of cryptocurrencies.`,
		},
		{
			name: 'WGG Form',
			link: 'https://github.com/bytesizedpcs/WGGForm',
			description: `an application created in React to handle form submissions. `,
		},
		{
			name: 'Twitch Name Finder',
			link: 'https://github.com/bytesizedpcs/Twitch-Valid-Usernames',
			description: `an application created in Python to search bulk names for Twitch.tv. `,
		},
		{
			name: 'Slack Clone',
			link: 'https://github.com/bytesizedpcs/SlackClone',
			description: `a Slack clone written in Node.js with a GraphQL layer. `,
		},
		{
			name: 'Supreme.py',
			link: '#',
			description: `Supreme.py was an open-sourced Supreme auto-checkout program.`,
		},
	]
	const links = [
    {
      name: 'resume',
      link: 'https://docs.google.com/document/d/1PtGT1UWIKTlYa1shB7kMjW1VkFTC2hqEygesXUKhPIc/edit?usp=sharing',
    },
		{
			name: 'twitter',
			link: 'https://twitter.com/cccanadaaa',
		},
		{
			name: 'github',
			link: 'https://github.com/bytesizedpcs',
		},
		{
			name: 'linkedin',
			link: 'https://linkedin.com/in/austin-canada',
		},
		{
			name: 'email',
			link: 'theaustincanada@gmail.com',
		},
	]
	const jobTitle = 'web developer';
</script>

<style>
	a {
		font-size: var(--main-font-size);
		color: var(--main-fg-color);
		text-decoration: underline dotted;

		padding-top: 1px;
		padding-left: 0;
		padding-bottom: 3px;

		margin-right: 3px;
	}

	a:hover {
		/* background-color: var(--main-bg-color); */
		/*border: 1px solid var(--main-fg-color);*/
		/*color: var(--fg-lighter-color);*/
		text-decoration: underline dashed;
		transition: 0.1s;
	}

	p {
		font-size: var(--main-font-size);
		color: var(--main-fg-color);
		text-decoration: underline dotted;

		padding-top: 1px;
		padding-left: 0;
		padding-bottom: 3px;

		margin-right: 3px;
	}

	span {
		font-size: var(--main-font-size);
	}

	h3 {
		font-family: 'SF Mono Semibold';
		margin: 0;
		padding: 0;
	}

	h4 {
		font-family: 'SF Mono Semibold';
		margin-bottom: 0;
		padding-bottom: 0;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	li {
		margin-bottom: 2px;
		list-style: none;
	}

	span {
		color: var(--fg-lighter-color);
	}

	.item-container { 
		margin-bottom: 1em;
	}

	.header {
		font-family: 'SF Mono Semibold';
	}

	#job-title {
		font-family: 'SF Mono';
		color: var(--fg-lighter-color);
		padding: 0;
		margin: 0;
		margin-bottom: 1em;
	}

	#name { 
		margin-top: 1em;
		color: #161616;
	}
</style>

<svelte:head>
	<title>austin canada</title>
</svelte:head>

<h3 id="name">austin canada</h3>
<h4 id="job-title">{jobTitle}</h4>

<div class="item-container">
	<h4 class="header">projects</h4>
	<ul>
		{#each projects as project}
		<li><a href={project.link} target="_blank">{project.name}</a><span>: {project.description}</span></li>
		{/each}
	</ul>
</div>

<div class="item-container">
	<h4 class="header">links</h4>
	<ul>
		{#each links as link}
      {#if link.name === "email"}
		    <li><a href="mailto: {link.link}" target="_blank">{link.link}</a></li>
      {:else}
		    <li><a href={link.link} target="_blank">{link.name}</a></li>
      {/if}
		{/each}
	</ul>
</div>
