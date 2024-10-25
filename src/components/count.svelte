<script lang="ts">
	const { class: className = "" } = $props()
	let count = $state(0)
	let double = $derived(count * 2)

	$effect(() => console.log(`count: ${count}, double: ${double}`))
</script>

<div class={className}>
	<div>
		<h1>Count Component</h1>
		<h2>$props</h2>
		<p class="muted">{`const {class: className = ""} = $props()`}</p>
		<p>Component accepts props: ["class"]</p>
	</div>

	<div>
		<h2>$state</h2>
		<p class="muted">let count = $state(0)</p>
		<p>Creates reactive variable</p>
		<samp>count: {count}</samp>
	</div>

	<div>
		<h2>$derived</h2>
		<p class="muted">let double = $derived(count * 2)</p>
		<p>Updates the state when count changes</p>
		<samp>double: {double}</samp>
	</div>

	<div>
		<h2>$effect</h2>
		<p class="muted">{`$effect(() => console.log(\`count: \${count}, double: \${double}\`))`}</p>
		<p>Logs when count or double changes</p>
	</div>

	<div class="grid grid-cols-2 gap-2">
		<div class="flex flex-col gap-1">
			<button onclick={() => count--}> - </button>
			<p class="muted">{`onclick={() => count--}`}</p>
		</div>
		<div class="flex flex-col gap-1">
			<button onclick={() => count++}> + </button>
			<p class="muted">{`onclick={() => count++}`}</p>
		</div>
	</div>
</div>
