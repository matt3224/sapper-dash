<style>
	
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<h1>Dash test</h1>

<video playsinline autoplay muted loop bind:this="{video}"></video>

<p><strong>Try editing this file (src/routes/index.svelte) to test live reloading.</strong></p>

<script>
	import dashjs from 'dashjs';
	import { onMount } from 'svelte';

	let video;

	onMount(() => {
		let player = dashjs.MediaPlayer().create();
         player.initialize(video, `https://videodelivery.net/6eacc1e5e33739494095da1827437f4b/manifest/video.mpd`, true);
	})
</script>
