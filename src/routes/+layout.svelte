<script lang="ts">
	import '../app.css';
	import { dev } from '$app/environment';
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	import Head from '$lib/components/Head.svelte';

	injectAnalytics({ mode: dev ? 'development' : 'production' });
	injectSpeedInsights();
	let { children } = $props();
</script>

<Head/>

{@render children()}
