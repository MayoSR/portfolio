<script>
	import Projects from "./Projects.svelte";
	import Intro from "./Intro.svelte";
	import JobApp from "./JobApp.svelte";
	import Home from "./Home.svelte";
	import { page } from "./stores.js";
	import { Router, Link, Route } from "svelte-routing";
	export let url = "";
</script>

<div id="main-div">
	<Router {url}>
		<div>
			<Route path="job"><JobApp /></Route>
			<Route path="/"><Home /></Route>
		</div>
	</Router>
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		background: #212121;
		color: #fff;
	}
</style>
