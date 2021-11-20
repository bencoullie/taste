<script context="module">
	/** @type {import('@sveltejs/kit').ErrorLoad} */
	export function load({ error, status }) {
		return {
			props: {
				title: `${status}: ${error.message}`
			}
		};
	}
</script>

<script>
	export let title;
</script>

<h1>Whoops something went wrong.</h1>
<h3>{title}</h3>

<style>
	h3 {
		color: red;
	}
</style>