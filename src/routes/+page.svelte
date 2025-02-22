<script>
	import Navbar from '$lib/components/Navbar.svelte';

	const projects = [
		{
			name: 'Lofi-Box',
			url: 'https://github.com/sharukhi/lofi-box',
			description:
				'Lofi-Box is a Chrome extension that delivers seamless lo-fi audio directly within your browser. Designed for minimal resource usage, it provides a lightweight, non-intrusive ambient soundscape to enhance focus while working, studying, or browsing.'
		},
		{
			name: 'Khobor',
			url: 'https://github.com/sharukhi/khobor',
			description:
				'Khobor, which means “news” in Bengali, is a simple and focused news app that keeps you updated on everything happening in Bangladesh. It’s designed to give you the news clearly and concisely—no distractions, no clutter, just the important updates you need.'
		},
		{
			name: 'DriveSafe',
			url: 'https://github.com/sharukhi/drivesafe',
			description:
				'Driver drowsiness is a leading cause of road accidents, and DriveSafe helps prevent it. Built in Python, this system uses computer vision to monitor drivers in real time, detecting signs of fatigue. If drowsiness is detected, it triggers alerts to keep the driver awake and focused.'
		},
		{
			name: 'OAB',
			url: 'https://github.com/sharukhi/oab',
			description:
				'Object Avoiding Bot, or OAB, is a robotics project using very simple hardware and simple programming logic. The robot is able to detect obstacles around itself and avoid obstacles in real time using an Arduino board and a few other essential components.'
		}
	];
</script>

<svelte:head>
  <title>Home | Sharukhi</title>
</svelte:head>


<div class="mx-auto max-w-3xl px-4 py-8">
	<Navbar />
	<section>
		<h2 class="mb-8 text-lg font-semibold">Projects</h2>
		<div class="space-y-8">
			{#each projects as project}
				<div>
					<a href={project.url} class="font-semibold underline">
						{project.name}
					</a>
					<p class="mt-2 text-gray-700 dark:text-gray-300">{project.description}</p>
				</div>
			{/each}
		</div>
	</section>
</div>
