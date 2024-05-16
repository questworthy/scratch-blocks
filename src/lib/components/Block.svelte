<script>
	export let type = 'action'; // or "event" block

	// props for action block
	export let fill = '#9966FF';
	export let stroke = '#774DCB';
	export let width = '280';
</script>

<div class="h-20">
	{#if type === 'event'}
		<svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" class="bg-sky-200">
			<g transform="translate(10,20)">
				<path
					class=""
					stroke="#CC9900"
					fill="#FFBF00"
					d="m 0,0 c 25,-22 71,-22 96,0 H 140 a 4,4 0 0,1 4,4 v 40  a 4,4 0 0,1 -4,4 H 48 c -2,0 -3,1 -4,2 l -4,4 c -1,1 -2,2 -4,2 h -12 c -2,0 -3,-1 -4,-2 l -4,-4 c -1,-1 -2,-2 -4,-2 H 4 a 4,4 0 0,1 -4,-4 z"
				></path>
			</g>
		</svg>
	{:else}
		<svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" class="bg-sky-200">
			<g transform="translate(10,15)">
				<path
					{stroke}
					{fill}
					d="m 0,4 A 4,4 0 0,1 4,0 H 12 c 2,0 3,1 4,2 l 4,4 c 1,1 2,2 4,2 h 12 c 2,0 3,-1 4,-2 l 4,-4 c 1,-1 2,-2 4,-2 H {width} a 4,4 0 0,1 4,4 v 40  a 4,4 0 0,1 -4,4 H 48   c -2,0 -3,1 -4,2 l -4,4 c -1,1 -2,2 -4,2 h -12 c -2,0 -3,-1 -4,-2 l -4,-4 c -1,-1 -2,-2 -4,-2 H 4 a 4,4 0 0,1 -4,-4 z"
				></path>
			</g>
		</svg>
	{/if}
</div>
