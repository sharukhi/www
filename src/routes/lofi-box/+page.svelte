<script>
	import SubmitJSON from 'submitjson'
	import { PUBLIC_SUBMIT_JSON_API_KEY } from '$env/static/public'
	import { PUBLIC_SUBMIT_JSON_ENDPOINT } from '$env/static/public'

	// Extension details - customize these
	const extensionName = "Lofi-Box";
	const tagline = "Focus with lofi Beats";
	const description = "Simple lofi music player for your browser";
	
	// Features list with icons
	const features = [
	  {
		title: "Fast",
		description: "Play LoFi beats instantly with zero delays.",
		icon: "zap"
	  },
	  {
		title: "Lightweight",
		description: "Minimal impact on performance for a smooth experience.",
		icon: "shield"
	  },
	  {
		title: "Open Source",
		description: "Fully transparent, customizable, and community-supported.",
		icon: "settings"
	  }
	];
  
	// Reviews/Testimonials
	const reviews = [
	  {
		name: "Britney Lau",
		avatar: "/projects/lofi-box/review_avatar_1.jpg",
		rating: 5,
		text: "I love it I no longer need to open Youtube and have to swallow ads just by searching Lofi Music",
		link: "https://chromewebstore.google.com/reviews/4b211cd3-26db-4015-9337-748c35fcda69"
	},
	  {
		name: "Sadikin Hamim",
		avatar: "/projects/lofi-box/review_avatar_2.jpg",
		rating: 4,
		text: "Found it useful",
		link: "https://chromewebstore.google.com/reviews/b61b2e78-c001-4730-868a-e1d4454e4c7a"
	},
	  {
		name: "Jarif Azmain",
		avatar: "/projects/lofi-box/review_avatar_3.jpg",
		rating: 4,
		text: "Just what I needed. Perfect for studying or chilling, and it works so smoothly!",
		link: "/"
	  }
	];
  
	// Mobile menu state
	let mobileMenuOpen = false;
	const toggleMobileMenu = () => {
	  mobileMenuOpen = !mobileMenuOpen;
	};
  
	// Newsletter form
	let email = "";
	const handleSubscribe = () => {
	  if (email) {
		alert(`Thanks for subscribing with ${email}!`);
		email = "";
	  }
	};

	const sj = new SubmitJSON({ apiKey: PUBLIC_SUBMIT_JSON_API_KEY, endpoint: PUBLIC_SUBMIT_JSON_ENDPOINT })

let form_email = ''

async function submit() {
  await sj.submit({ form_email })
}
  </script>
  
  <main class="min-h-screen bg-white text-gray-900 font-sans">
	<header class="container mx-auto px-4 py-6">
	<div class="flex justify-between items-center">
	  <div class="flex items-center gap-2">
		<div class="w-8 h-">
		  <img src="/projects/lofi-box/logo.png" alt="" srcset="">
		</div>
		<h1 class="text-xl font-bold">{extensionName}</h1>
	  </div>
	  
	  <!-- Desktop Navigation -->
	  <nav class="hidden md:flex items-center gap-6">
		<a href="#features" class="text-sm hover:text-gray-600 transition-colors">Features</a>
		<a href="#reviews" class="text-sm hover:text-gray-600 transition-colors">Reviews</a>
		<a href="https://github.com/sharukhi/lofi-box" target="_blank" rel="noopener noreferrer" 
		   class="flex items-center gap-1 text-sm hover:text-gray-600 transition-colors">
		  GitHub
		</a>
	  </nav>
  
	  <!-- Mobile Menu Button -->
	  <button class="md:hidden" on:click={toggleMobileMenu} aria-label="Toggle menu">
		<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={mobileMenuOpen ? "hidden" : "block"}>
		  <line x1="4" x2="20" y1="12" y2="12"></line>
		  <line x1="4" x2="20" y1="6" y2="6"></line>
		  <line x1="4" x2="20" y1="18" y2="18"></line>
		</svg>
		<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={mobileMenuOpen ? "block" : "hidden"}>
		  <path d="M18 6 6 18"></path>
		  <path d="m6 6 12 12"></path>
		</svg>
	  </button>
	</div>
  
	<!-- Mobile Navigation -->
	{#if mobileMenuOpen}
	  <nav class="md:hidden mt-4 py-4 flex flex-col gap-4 border-t">
		<a href="#features" class="text-sm hover:text-gray-600 transition-colors" on:click={toggleMobileMenu}>Features</a>
		<a href="#reviews" class="text-sm hover:text-gray-600 transition-colors" on:click={toggleMobileMenu}>Reviews</a>
		<a href="https://github.com/sharukhi/lofi-box" target="_blank" rel="noopener noreferrer" 
		   class="flex items-center gap-1 text-sm hover:text-gray-600 transition-colors">
		  GitHub
		</a>
	  </nav>
	{/if}
  </header>
  
	<section class="container mx-auto px-4 py-16 md:py-24">
	  <div class="max-w-3xl mx-auto text-center">
		<h2 class="text-4xl md:text-5xl font-bold mb-6 bg-gradient-to-r from-orange-400 to-pink-500 text-transparent bg-clip-text">{tagline}</h2>
		<p class="text-lg text-gray-600 mb-8">{description}</p>
		
		<div class="flex flex-wrap justify-center gap-4 mb-[8%]">
		  <a href="https://chromewebstore.google.com/detail/lofi-box/fbogegnhfhlbdjjhompihcgcenhdclhj" target="_blank" class="flex items-center gap-2 px-6 py-3 bg-white border border-gray-300 text-gray-900 rounded-lg hover:bg-gray-50 transition-colors">
			<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 256 256"><path fill="#fff" d="M128.003 199.216c39.335 0 71.221-31.888 71.221-71.223S167.338 56.77 128.003 56.77S56.78 88.658 56.78 127.993s31.887 71.223 71.222 71.223"/><path fill="#229342" d="M35.89 92.997Q27.92 79.192 17.154 64.02a127.98 127.98 0 0 0 110.857 191.981q17.671-24.785 23.996-35.74q12.148-21.042 31.423-60.251v-.015a63.993 63.993 0 0 1-110.857.017Q46.395 111.19 35.89 92.998"/><path fill="#fbc116" d="M128.008 255.996A127.97 127.97 0 0 0 256 127.997A128 128 0 0 0 238.837 64q-36.372-3.585-53.686-3.585q-19.632 0-57.152 3.585l-.014.01a63.99 63.99 0 0 1 55.444 31.987a63.99 63.99 0 0 1-.001 64.01z"/><path fill="#1a73e8" d="M128.003 178.677c27.984 0 50.669-22.685 50.669-50.67s-22.685-50.67-50.67-50.67c-27.983 0-50.669 22.686-50.669 50.67s22.686 50.67 50.67 50.67"/><path fill="#e33b2e" d="M128.003 64.004H238.84a127.973 127.973 0 0 0-221.685.015l55.419 95.99l.015.008a63.993 63.993 0 0 1 55.415-96.014z"/></svg>
			Add to Chrome
		  </a>
		  <a href="https://addons.mozilla.org/en-US/firefox/addon/lofi-box/" target="_blank" class="flex items-center gap-2 px-6 py-3 bg-white border border-gray-300 text-gray-900 rounded-lg hover:bg-gray-50 transition-colors">
			<svg xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 256 265"><defs><radialGradient id="logosFirefox0" cx="-7907.187" cy="-8515.121" r="80.797" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".129" stop-color="#ffbd4f"/><stop offset=".186" stop-color="#ffac31"/><stop offset=".247" stop-color="#ff9d17"/><stop offset=".283" stop-color="#ff980e"/><stop offset=".403" stop-color="#ff563b"/><stop offset=".467" stop-color="#ff3750"/><stop offset=".71" stop-color="#f5156c"/><stop offset=".782" stop-color="#eb0878"/><stop offset=".86" stop-color="#e50080"/></radialGradient><radialGradient id="logosFirefox1" cx="-7936.711" cy="-8482.089" r="80.797" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".3" stop-color="#960e18"/><stop offset=".351" stop-color="#b11927" stop-opacity="0.74"/><stop offset=".435" stop-color="#db293d" stop-opacity="0.343"/><stop offset=".497" stop-color="#f5334b" stop-opacity="0.094"/><stop offset=".53" stop-color="#ff3750" stop-opacity="0"/></radialGradient><radialGradient id="logosFirefox2" cx="-7926.97" cy="-8533.457" r="58.534" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".132" stop-color="#fff44f"/><stop offset=".252" stop-color="#ffdc3e"/><stop offset=".506" stop-color="#ff9d12"/><stop offset=".526" stop-color="#ff980e"/></radialGradient><radialGradient id="logosFirefox3" cx="-7945.648" cy="-8460.984" r="38.471" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".353" stop-color="#3a8ee6"/><stop offset=".472" stop-color="#5c79f0"/><stop offset=".669" stop-color="#9059ff"/><stop offset="1" stop-color="#c139e6"/></radialGradient><radialGradient id="logosFirefox4" cx="-7935.62" cy="-8491.546" r="20.397" gradientTransform="matrix(3.21411 -.77707 .90934 3.76302 33365.914 25904.014)" gradientUnits="userSpaceOnUse"><stop offset=".206" stop-color="#9059ff" stop-opacity="0"/><stop offset=".278" stop-color="#8c4ff3" stop-opacity="0.064"/><stop offset=".747" stop-color="#7716a8" stop-opacity="0.45"/><stop offset=".975" stop-color="#6e008b" stop-opacity="0.6"/></radialGradient><radialGradient id="logosFirefox5" cx="-7937.731" cy="-8518.427" r="27.676" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#ffe226"/><stop offset=".121" stop-color="#ffdb27"/><stop offset=".295" stop-color="#ffc82a"/><stop offset=".502" stop-color="#ffa930"/><stop offset=".732" stop-color="#ff7e37"/><stop offset=".792" stop-color="#ff7139"/></radialGradient><radialGradient id="logosFirefox6" cx="-7915.977" cy="-8535.981" r="118.081" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".113" stop-color="#fff44f"/><stop offset=".456" stop-color="#ff980e"/><stop offset=".622" stop-color="#ff5634"/><stop offset=".716" stop-color="#ff3647"/><stop offset=".904" stop-color="#e31587"/></radialGradient><radialGradient id="logosFirefox7" cx="-7927.165" cy="-8522.859" r="86.499" gradientTransform="matrix(.3472 3.29017 -2.15928 .22816 -15491.597 28008.376)" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#fff44f"/><stop offset=".06" stop-color="#ffe847"/><stop offset=".168" stop-color="#ffc830"/><stop offset=".304" stop-color="#ff980e"/><stop offset=".356" stop-color="#ff8b16"/><stop offset=".455" stop-color="#ff672a"/><stop offset=".57" stop-color="#ff3647"/><stop offset=".737" stop-color="#e31587"/></radialGradient><radialGradient id="logosFirefox8" cx="-7938.383" cy="-8508.176" r="73.72" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".137" stop-color="#fff44f"/><stop offset=".48" stop-color="#ff980e"/><stop offset=".592" stop-color="#ff5634"/><stop offset=".655" stop-color="#ff3647"/><stop offset=".904" stop-color="#e31587"/></radialGradient><radialGradient id="logosFirefox9" cx="-7918.923" cy="-8503.861" r="80.686" gradientTransform="translate(26367.938 28186.305)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".094" stop-color="#fff44f"/><stop offset=".231" stop-color="#ffe141"/><stop offset=".509" stop-color="#ffaf1e"/><stop offset=".626" stop-color="#ff980e"/></radialGradient><linearGradient id="logosFirefoxa" x1="70.786" x2="6.447" y1="12.393" y2="74.468" gradientTransform="translate(-2.999 -.01)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".048" stop-color="#fff44f"/><stop offset=".111" stop-color="#ffe847"/><stop offset=".225" stop-color="#ffc830"/><stop offset=".368" stop-color="#ff980e"/><stop offset=".401" stop-color="#ff8b16"/><stop offset=".462" stop-color="#ff672a"/><stop offset=".534" stop-color="#ff3647"/><stop offset=".705" stop-color="#e31587"/></linearGradient><linearGradient id="logosFirefoxb" x1="70.013" x2="15.267" y1="12.061" y2="66.806" gradientTransform="translate(-2.999 -.01)scale(3.3067)" gradientUnits="userSpaceOnUse"><stop offset=".167" stop-color="#fff44f" stop-opacity="0.8"/><stop offset=".266" stop-color="#fff44f" stop-opacity="0.634"/><stop offset=".489" stop-color="#fff44f" stop-opacity="0.217"/><stop offset=".6" stop-color="#fff44f" stop-opacity="0"/></linearGradient></defs><path fill="url(#logosFirefoxa)" d="M248.033 88.713c-5.569-13.399-16.864-27.866-25.71-32.439a133.2 133.2 0 0 1 12.979 38.9l.023.215c-14.49-36.126-39.062-50.692-59.13-82.41a155 155 0 0 1-3.019-4.907a41 41 0 0 1-1.412-2.645a23.3 23.3 0 0 1-1.912-5.076a.33.33 0 0 0-.291-.331a.5.5 0 0 0-.241 0c-.016 0-.043.03-.063.037s-.063.036-.092.049l.049-.086c-32.19 18.849-43.113 53.741-44.118 71.194a64.1 64.1 0 0 0-35.269 13.593a38 38 0 0 0-3.307-2.506a59.4 59.4 0 0 1-.36-31.324a94.9 94.9 0 0 0-30.848 23.841h-.06c-5.079-6.438-4.722-27.667-4.431-32.102a23 23 0 0 0-4.279 2.272a93.4 93.4 0 0 0-12.526 10.73a112 112 0 0 0-11.98 14.375v.019v-.023A108.3 108.3 0 0 0 4.841 108.92l-.171.846a204 204 0 0 0-1.26 8.003c0 .096-.02.185-.03.281a122 122 0 0 0-2.08 17.667v.662c.086 98.661 106.944 160.23 192.344 110.825a128.17 128.17 0 0 0 62.12-89.153c.215-1.653.39-3.29.582-4.96a131.8 131.8 0 0 0-8.313-64.378M100.322 189.031c.599.288 1.161.599 1.776.873l.089.057a69 69 0 0 1-1.865-.93m135.013-93.612v-.123l.023.136z"/><path fill="url(#logosFirefox0)" d="M248.033 88.713c-5.569-13.399-16.864-27.866-25.71-32.439a133.2 133.2 0 0 1 12.979 38.9v.122l.023.136a116.07 116.07 0 0 1-3.988 86.497c-14.688 31.516-50.242 63.819-105.894 62.248c-60.132-1.703-113.089-46.323-122.989-104.766c-1.802-9.216 0-13.888.906-21.378a95.4 95.4 0 0 0-2.06 17.684v.662c.086 98.661 106.944 160.23 192.344 110.825a128.17 128.17 0 0 0 62.12-89.153c.215-1.653.39-3.29.582-4.96a131.8 131.8 0 0 0-8.313-64.378"/><path fill="url(#logosFirefox1)" d="M248.033 88.713c-5.569-13.399-16.864-27.866-25.71-32.439a133.2 133.2 0 0 1 12.979 38.9v.122l.023.136a116.07 116.07 0 0 1-3.988 86.497c-14.688 31.516-50.242 63.819-105.894 62.248c-60.132-1.703-113.089-46.323-122.989-104.766c-1.802-9.216 0-13.888.906-21.378a95.4 95.4 0 0 0-2.06 17.684v.662c.086 98.661 106.944 160.23 192.344 110.825a128.17 128.17 0 0 0 62.12-89.153c.215-1.653.39-3.29.582-4.96a131.8 131.8 0 0 0-8.313-64.378"/><path fill="url(#logosFirefox2)" d="M185.754 103.778c.278.195.536.39.797.585a69.8 69.8 0 0 0-11.904-15.525C134.815 48.999 164.208 2.457 169.165.093l.049-.073c-32.19 18.849-43.113 53.741-44.118 71.194c1.495-.103 2.976-.229 4.504-.229a64.68 64.68 0 0 1 56.154 32.793"/><path fill="url(#logosFirefox3)" d="M129.683 111.734c-.212 3.188-11.475 14.182-15.413 14.182c-36.443 0-42.359 22.046-42.359 22.046c1.614 18.564 14.55 33.854 30.187 41.942c.714.371 1.439.705 2.163 1.032a71 71 0 0 0 3.763 1.541a57 57 0 0 0 16.675 3.217c63.876 2.996 76.25-76.384 30.154-99.419a44.24 44.24 0 0 1 30.901 7.503A64.68 64.68 0 0 0 129.6 70.985c-1.521 0-3.009.126-4.504.229a64.1 64.1 0 0 0-35.269 13.593c1.954 1.654 4.16 3.863 8.806 8.442c8.696 8.568 31 17.443 31.05 18.485"/><path fill="url(#logosFirefox4)" d="M129.683 111.734c-.212 3.188-11.475 14.182-15.413 14.182c-36.443 0-42.359 22.046-42.359 22.046c1.614 18.564 14.55 33.854 30.187 41.942c.714.371 1.439.705 2.163 1.032a71 71 0 0 0 3.763 1.541a57 57 0 0 0 16.675 3.217c63.876 2.996 76.25-76.384 30.154-99.419a44.24 44.24 0 0 1 30.901 7.503A64.68 64.68 0 0 0 129.6 70.985c-1.521 0-3.009.126-4.504.229a64.1 64.1 0 0 0-35.269 13.593c1.954 1.654 4.16 3.863 8.806 8.442c8.696 8.568 31 17.443 31.05 18.485"/><path fill="url(#logosFirefox5)" d="M83.852 80.545a82 82 0 0 1 2.645 1.756a59.4 59.4 0 0 1-.36-31.324a94.9 94.9 0 0 0-30.849 23.841c.625-.017 19.216-.351 28.564 5.727"/><path fill="url(#logosFirefox6)" d="M2.471 139.411c9.89 58.443 62.857 103.063 122.989 104.766c55.652 1.574 91.205-30.732 105.894-62.248a116.07 116.07 0 0 0 3.988-86.497v-.122c0-.096-.02-.153 0-.123l.023.215c4.547 29.684-10.552 58.443-34.155 77.889l-.073.166c-45.989 37.455-90.002 22.598-98.91 16.533a65 65 0 0 1-1.865-.929c-26.814-12.817-37.891-37.247-35.517-58.198a32.91 32.91 0 0 1-30.359-19.096a48.34 48.34 0 0 1 47.117-1.891a63.82 63.82 0 0 0 48.119 1.891c-.049-1.042-22.353-9.92-31.05-18.484c-4.646-4.58-6.851-6.786-8.805-8.442a38 38 0 0 0-3.307-2.507c-.761-.519-1.617-1.081-2.645-1.756c-9.348-6.078-27.939-5.744-28.554-5.727h-.059c-5.079-6.438-4.722-27.667-4.431-32.101a23 23 0 0 0-4.279 2.271a93.4 93.4 0 0 0-12.526 10.73a112 112 0 0 0-12.03 14.342v.019v-.023A108.3 108.3 0 0 0 4.841 108.92c-.062.261-4.616 20.167-2.37 30.491"/><path fill="url(#logosFirefox7)" d="M174.654 88.838a69.8 69.8 0 0 1 11.904 15.542a27 27 0 0 1 1.921 1.574c29.056 26.784 13.832 64.646 12.698 67.341c23.603-19.447 38.688-48.205 34.155-77.89c-14.497-36.142-39.069-50.708-59.137-82.426a155 155 0 0 1-3.019-4.907a41 41 0 0 1-1.412-2.645a23.3 23.3 0 0 1-1.912-5.076a.33.33 0 0 0-.291-.331a.5.5 0 0 0-.241 0c-.016 0-.043.03-.063.037s-.063.036-.092.049c-4.957 2.351-34.35 48.893 5.489 88.732"/><path fill="url(#logosFirefox8)" d="M188.459 105.937a27 27 0 0 0-1.921-1.574c-.261-.195-.519-.39-.797-.585a44.24 44.24 0 0 0-30.901-7.503c46.095 23.048 33.728 102.415-30.154 99.419a57 57 0 0 1-16.675-3.217a67 67 0 0 1-3.763-1.541c-.725-.331-1.449-.661-2.163-1.032l.089.057c8.908 6.081 52.907 20.938 98.91-16.534l.073-.165c1.147-2.679 16.371-40.55-12.698-67.325"/><path fill="url(#logosFirefox9)" d="M71.911 147.962s5.916-22.046 42.359-22.046c3.938 0 15.211-10.994 15.413-14.182a63.82 63.82 0 0 1-48.119-1.892a48.34 48.34 0 0 0-47.118 1.892a32.91 32.91 0 0 0 30.359 19.096c-2.374 20.955 8.703 45.385 35.517 58.198c.599.288 1.161.599 1.776.873c-15.65-8.085-28.573-23.375-30.187-41.939"/><path fill="url(#logosFirefoxb)" d="M248.033 88.713c-5.569-13.399-16.864-27.866-25.71-32.439a133.2 133.2 0 0 1 12.979 38.9l.023.215c-14.49-36.126-39.062-50.692-59.13-82.41a155 155 0 0 1-3.019-4.907a41 41 0 0 1-1.412-2.645a23.3 23.3 0 0 1-1.912-5.076a.33.33 0 0 0-.291-.331a.5.5 0 0 0-.241 0c-.016 0-.043.03-.063.037s-.063.036-.092.049l.049-.086c-32.19 18.849-43.113 53.741-44.118 71.194c1.495-.103 2.976-.229 4.504-.229a64.68 64.68 0 0 1 56.154 32.793a44.24 44.24 0 0 0-30.901-7.503c46.096 23.048 33.729 102.415-30.154 99.419a57 57 0 0 1-16.675-3.217a67 67 0 0 1-3.763-1.541c-.724-.331-1.449-.661-2.163-1.032l.089.057a69 69 0 0 1-1.865-.93c.599.288 1.161.599 1.776.873c-15.65-8.088-28.573-23.378-30.187-41.942c0 0 5.916-22.046 42.359-22.046c3.938 0 15.211-10.994 15.413-14.182c-.05-1.042-22.354-9.92-31.05-18.485c-4.646-4.579-6.852-6.785-8.806-8.442a38 38 0 0 0-3.307-2.506a59.4 59.4 0 0 1-.36-31.324a94.9 94.9 0 0 0-30.848 23.841h-.06c-5.079-6.438-4.722-27.667-4.431-32.102a23 23 0 0 0-4.279 2.272a93.4 93.4 0 0 0-12.526 10.73a112 112 0 0 0-11.98 14.375v.019v-.023A108.3 108.3 0 0 0 4.841 108.92l-.171.846c-.242 1.128-1.323 6.855-1.479 8.085c0 .093 0-.096 0 0A149 149 0 0 0 1.3 135.717v.662c.086 98.661 106.944 160.23 192.344 110.825a128.17 128.17 0 0 0 62.12-89.153c.215-1.653.39-3.29.582-4.96a131.8 131.8 0 0 0-8.313-64.378m-12.715 6.583l.024.136z"/></svg>
			Add to Firefox
		  </a>
		</div>
	  </div>
	  
	</section>
	
	<section id="features" class="py-16">
	<div class="container mx-auto px-4">
	  <h3 class="text-2xl font-bold text-center mb-12">Features</h3>
	  
	  <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-4xl mx-auto">
		{#each features as feature}
		  <div class="p-6 bg-white rounded-lg ">
			<div class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center mb-4">
			  {#if feature.icon === "zap"}
				<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"></polygon></svg>
			  {:else if feature.icon === "shield"}
				<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path></svg>
			  {:else if feature.icon === "settings"}
				<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12.22 2h-.44a2 2 0 0 0-2 2v.18a2 2 0 0 1-1 1.73l-.43.25a2 2 0 0 1-2 0l-.15-.08a2 2 0 0 0-2.73.73l-.22.38a2 2 0 0 0 .73 2.73l.15.1a2 2 0 0 1 1 1.72v.51a2 2 0 0 1-1 1.74l-.15.09a2 2 0 0 0-.73 2.73l.22.38a2 2 2 0 0 0 2.73.73l.15-.08a2 2 0 0 1 2 0l.43.25a2 2 0 0 1 1 1.73V20a2 2 0 0 0 2 2h.44a2 2 0 0 0 2-2v-.18a2 2 0 0 1 1-1.73l.43-.25a2 2 0 0 1 2 0l.15.08a2 2 0 0 0 2.73-.73l.22-.39a2 2 0 0 0-.73-2.73l-.15-.08a2 2 0 0 1-1-1.74v-.5a2 2 0 0 1 1-1.74l.15-.09a2 2 0 0 0 .73-2.73l-.22-.38a2 2 0 0 0-2.73-.73l-.15.08a2 2 0 0 1-2 0l-.43-.25a2 2 0 0 1-1-1.73V4a2 2 0 0 0-2-2z"></path><circle cx="12" cy="12" r="3"></circle></svg>
			  {/if}
			</div>
			<h4 class="text-xl font-semibold mb-2">{feature.title}</h4>
			<p class="text-gray-600">{feature.description}</p>
		  </div>
		{/each}
	  </div>
	  
	</div>
  </section>
	
	<section id="reviews" class="py-16">
	<div class="container mx-auto px-4">
	  <h3 class="text-2xl font-bold text-center mb-12">What Our Users Say</h3>
	  
	  <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-4xl mx-auto">
		{#each reviews as review}
		<a href={review.link} target="_blank">
		  <div class="p-6 bg-white rounded-lg  border border-gray-100">
			<div class="flex items-center gap-3 mb-4">
			  <div>
				<img class="rounded-full h-14" src={review.avatar} alt=""  srcset="">
			  </div>
			  <div>
				<p class="font-medium">{review.name}</p>
				<div class="flex">
				  {#each Array(5) as _, i}
					<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill={i < review.rating ? "currentColor" : "none"} stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={i < review.rating ? "text-yellow-500" : "text-gray-300"}>
					  <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon>
					</svg>
				  {/each}
				</div>
			  </div>
			</div>
			<p class="text-gray-600">{review.text}</p>
		  </div>
		</a>
		{/each}
	  </div>
	</div>
  </section>
	
	<section id="newsletter" class=" py-16">
	<div class="container mx-auto px-4">
	  <div class="max-w-xl mx-auto text-center">
		<h3 class="text-2xl font-bold mb-4">Stay Updated</h3>
		<p class="text-gray-600 mb-6">Subscribe to our newsletter to get updates on new features.</p>

		<form on:submit|preventDefault={submit} class="flex flex-col sm:flex-row gap-2">
			<input type="email" bind:value={form_email} placeholder="Enter your email" 
			class="flex-1 px-4 py-2 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-gray-900 focus:border-transparent"
			required>
			<button type="submit" class="px-6 py-2 bg-gray-900 text-white rounded-lg hover:bg-gray-800 transition-colors">
			  Submit
			</button>
		</form>
	  </div>
	</div>
  </section>
	
	<footer class="container mx-auto px-4 py-8 mt-12 text-center text-gray-600 text-sm">
	  <p>© {new Date().getFullYear()} <a href="/" class="underline">Sharukhi</a>. All rights reserved.</p>
	</footer>
  </main>