<script>
	import Block from './Block.svelte';

	const style = 'm-0 p-0 text-white';
	const stroke = '#BD42BD';
	const fill = '#CF63CF';

	export let withFlag = true;
</script>

{#if withFlag}
	<Block type="event" {fill} {stroke} width="180">
		<div class="absolute flex gap-2 items-center left-4 top-7">
			<p class={style}>
				when
				<img
					src="data:image/svg+xml;base64,PHN2ZyBpZD0iTGF5ZXJfMSIgZGF0YS1uYW1lPSJMYXllciAxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNi42MyAxNy41Ij48ZGVmcz48c3R5bGU+LmNscy0xLC5jbHMtMntmaWxsOiM0Y2JmNTY7c3Ryb2tlOiM0NTk5M2Q7c3Ryb2tlLWxpbmVjYXA6cm91bmQ7c3Ryb2tlLWxpbmVqb2luOnJvdW5kO30uY2xzLTJ7c3Ryb2tlLXdpZHRoOjEuNXB4O308L3N0eWxlPjwvZGVmcz48dGl0bGU+aWNvbi0tZ3JlZW4tZmxhZzwvdGl0bGU+PHBhdGggY2xhc3M9ImNscy0xIiBkPSJNLjc1LDJBNi40NCw2LjQ0LDAsMCwxLDguNDQsMmgwYTYuNDQsNi40NCwwLDAsMCw3LjY5LDBWMTIuNGE2LjQ0LDYuNDQsMCwwLDEtNy42OSwwaDBhNi40NCw2LjQ0LDAsMCwwLTcuNjksMCIvPjxsaW5lIGNsYXNzPSJjbHMtMiIgeDE9IjAuNzUiIHkxPSIxNi43NSIgeDI9IjAuNzUiIHkyPSIwLjc1Ii8+PC9zdmc+"
					alt=""
					class="m-0 p-0 text-white top-8 w-4 left-16 inline-block"
				/>
				clicked
			</p>
		</div>
	</Block>
{:else}
	<Block type="event" {fill} {stroke} width="250">
		<div class="absolute flex gap-2 items-center left-4 top-7">
			<p class={style}>when this sprite clicked</p>
		</div>
	</Block>
{/if}
