<script>
	import logo from '$lib/assets/logo.svg';

	const rickroll = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
	const linkStyle =
		'm-0 p-4 no-underline font-bold text-white h-full hover:bg-[#714EB6] content-center';

	let showBanner = true;
	let isOpen = false;
</script>

<!-- Navigation Bar ---------------------------------------------------------->

<div class="mt-0 h-16 bg-[#855CD6] flex justify-between items-center">
	<div class="flex justify-center items-center">
		<a href="https://scratch.mit.edu/">
			<img src={logo} alt="" class="m-0 mx-4 h-8" />
		</a>

		<a class={linkStyle} target="_blank" href={rickroll}> Home </a>
		<div class="p-0 m-0">
			<button
				on:click={() => {
					isOpen = !isOpen;
				}}
				on:copy
				class="{linkStyle} {isOpen && 'bg-[#714EB6]'}">Toolkits</button
			>
			{#if isOpen}
				<button class="block bg-[#855CD6] absolute m-0 p-0 text-left rounded-b-xl">
					<a href="#Scratch Basics" class="block {linkStyle}">Scratch Basics</a>
					<a href="#Gender Equity" class="block {linkStyle} rounded-b-xl">Gender Equity</a>
				</button>
			{/if}
		</div>
		<a class={linkStyle} target="_blank" href={rickroll}> About </a>
	</div>
	<a
		class="m-0 px-4 no-underline font-bold text-white h-full hover:bg-[#714EB6] content-center"
		href="https://scratch.mit.edu/"
	>
		Visit Scratch
	</a>
</div>

{#if showBanner}
	<div class="mt-0 h-16 bg-[#24603C] flex justify-between items-center text-white font-bold">
		<p class="m0 px-4 text-sm">
			✨ Quest Alliance has crafted this toolkit to facilitate your journey in learning Scratch.
		</p>
		<button
			class="mx-4 rounded-full bg-[#205636] p-2"
			on:click={() => {
				showBanner = false;
			}}
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="24"
				height="24"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
				class="lucide lucide-x"><path d="M18 6 6 18" /><path d="m6 6 12 12" /></svg
			>
		</button>
	</div>
{/if}

<!-- Landing content --------------------------------------------------------->

<div class="w-80 h-40">
	<svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" class="bg-red-200">
		<g transform="translate(10, 25)">
			<path
				class=""
				stroke="#CC9900"
				fill="#FFBF00"
				fill-opacity="1"
				d="m 0,0 c 25,-22 71,-22 96,0 H 260  a 4,4 0 0,1 4,4 v 40  a 4,4 0 0,1 -4,4 H 48   c -2,0 -3,1 -4,2 l -4,4 c -1,1 -2,2 -4,2 h -12 c -2,0 -3,-1 -4,-2 l -4,-4 c -1,-1 -2,-2 -4,-2 H 4 a 4,4 0 0,1 -4,-4 z"
			>
			</path>
			<text fill="white" stroke="white" stroke-width="0.5" transform="translate(10,30)">
				when this sprite clicked
			</text>
		</g>
		<g transform="translate(10, 74)">
			<path
				class="blocklyPath blocklyBlockBackground"
				stroke="#BD42BD"
				fill="#CF63CF"
				fill-opacity="1"
				d="m 0,4 A 4,4 0 0,1 4,0 H 12 c 2,0 3,1 4,2 l 4,4 c 1,1 2,2 4,2 h 12 c 2,0 3,-1 4,-2 l 4,-4 c 1,-1 2,-2 4,-2 H 220 a 4,4 0 0,1 4,4 v 40  a 4,4 0 0,1 -4,4 H 48   c -2,0 -3,1 -4,2 l -4,4 c -1,1 -2,2 -4,2 h -12 c -2,0 -3,-1 -4,-2 l -4,-4 c -1,-1 -2,-2 -4,-2 H 4 a 4,4 0 0,1 -4,-4 z"
			>
			</path>
			<g transform="translate(130,8)">
				<path
					transition:draw={{ duration: 5000, delay: 500, easing: quintOut }}
					stroke="#BD42BD"
					fill="#C94FC9"
					fill-opacity="1"
					d="m 0,0 m 16,0 H 60 a 16 16 0 0 1 0 32 H 16 a 16 16 0 0 1 0 -32 z"
				></path>
				<g class="blocklyEditableText" style="cursor: default;" transform="translate(8, 0) "
					><text
						x="25"
						y="18"
						fill="white"
						stroke="white"
						stroke-width="0.5"
						dominant-baseline="middle"
						dy="0"
						text-anchor="middle">Meow</text
					>
				</g>
			</g>

			<text fill="white" stroke="white" stroke-width="0.5" transform="translate(10,30)">
				start sound
			</text>
		</g>
	</svg>
</div>
