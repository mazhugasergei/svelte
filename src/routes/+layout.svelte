<script lang="ts">
	import "../app.css"
	let { children } = $props()
</script>

{@render children()}

<style lang="scss">
	:global(h1) {
		@apply text-3xl font-bold;
	}
	:global(h2) {
		@apply text-xl font-semibold;
	}
	:global(p) {
		@apply text-sm;
	}
	:global(p.muted) {
		@apply opacity-50;
	}

	:global(samp) {
		@apply inline bg-neutral-200 text-sm font-mono rounded px-2 py-1;
	}

	:global(button) {
		@apply bg-[#333] hover:bg-[#444] transition-colors text-white rounded-md px-4 py-1;
	}

	:global(code) {
		@apply block overflow-x-auto bg-[#333] text-white rounded p-2;
	}
	:global(pre) {
		@apply text-sm;
	}
</style>
