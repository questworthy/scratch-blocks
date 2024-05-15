<script>
	import logo from '$lib/assets/logo.svg';

	const rickroll = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
	const linkStyle =
		'm-0 p-4 no-underline font-bold text-white h-full hover:bg-[#714EB6] content-center';

	let showBanner = true;
	let isOpen = false;
</script>

<div class="mt-0 h-12 bg-[#855CD6] flex justify-between items-center text-xs">
	<div class="flex justify-center items-center">
		<a href="https://scratch.mit.edu/">
			<img src={logo} alt="" class="m-0 mx-4 h-[1.6rem]" />
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
