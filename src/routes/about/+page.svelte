<script>
	import Navbar from '$lib/components/Navbar.svelte';
</script>

<svelte:head>
  <title>About | Sharukhi</title>
</svelte:head>

<div class="mx-auto max-w-3xl px-4 py-8">
	<Navbar />

	<section>
		<div class="space-y-8">
			<div>
				<a href="/" class="font-semibold"> About </a>
				<p class="mt-2 text-gray-700 dark:text-gray-300">
          <p>Hello! I’m Sharukhi. Growing up, I taught myself how to do computer stuff and discovered that I really enjoy making things. That’s mostly it.
          Currently I’m mostly exploring this world of technology and working on my personal projects.
        </p>
        <br>
        <p>
          Feel free to write me — <a href="mailto:mail@sharukhi.xyz" class="underline">mail@sharukhi.xyz</a>

        </p>
			</div>
		</div>
	</section>
	<div class="mt-12">
		<p class="flex items-center gap-2">
		  Find me on
		  <span class="flex gap-4">
			<a href="https://github.com/sharukhi/"   target="_blank">
			  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
				<path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/>
				<path d="M9 18c-4.51 2-5-2-7-2"/>
			  </svg>
			  <span class="sr-only">GitHub</span>
			</a>
			<a href="https://x.com/sharukhi_"   target="_blank">
				<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 16 16"><path fill="currentColor" d="M9.294 6.928L14.357 1h-1.2L8.762 6.147L5.25 1H1.2l5.31 7.784L1.2 15h1.2l4.642-5.436L10.751 15h4.05zM7.651 8.852l-.538-.775L2.832 1.91h1.843l3.454 4.977l.538.775l4.491 6.47h-1.843z"/></svg>
			  <span class="sr-only">Twitter</span>
			</a>
			<a href="https://www.instagram.com/ataullah_sharukhi"   target="_blank">
			  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
				<rect width="20" height="20" x="2" y="2" rx="5" ry="5"/>
				<path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/>
				<line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/>
			  </svg>
			  <span class="sr-only">Instagram</span>
			</a>
			<a href="mailto:mail@sharukhi.xyz" target="_blank"  >
			  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
				<rect width="20" height="16" x="2" y="4" rx="2"/>
				<path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
			  </svg>
			  <span class="sr-only">Email</span>
			</a>
		  </span>
		</p>
	  </div>
</div>
