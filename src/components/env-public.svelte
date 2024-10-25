<script>
	import { env } from "$env/dynamic/public"

	const { class: className = "" } = $props()
</script>

<div class={className || ""}>
	<div>
		<h1>Env Public</h1>
		<p class="muted">{`import { env } from "$env/dynamic/public"`}</p>
	</div>

	<div>
		env:
		<pre><code>{JSON.stringify(env, null, 2)}</code></pre>
	</div>
</div>
