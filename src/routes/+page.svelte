<script>
	import logo from '$lib/assets/svelte-logo.png';
	let logos = [logo, logo, logo, logo, logo, logo, logo]; //로고 이미지 예시
</script>

<article class="pt-12 sm:pt-40 md:pt-20 lg:pt-24 xl:pt-40 flex items-center flex-col">
	<a href="/" class="flex items-center gap-x-2 bg-gray-100 p-px rounded border border-gray-200">
		<span class="text-xs text-white bg-indigo-600 px-1 rounded">NEW</span>
		<p class="text-xs">Raising €35 million ❞</p>
	</a>
	<h1 class="mt-5 text-3xl/tight sm:text-4xl/tight md:text-5xl/tight text-center text-balance">
		Financing solutions <br class="block sm:hidden" /> for your <br class="hidden sm:block" /> business
		customers.
	</h1>
	<h2 class="mt-8 text-sm md:text-md lg:text-lg text-center text-gray-400">
		Unlock a new revenue stream today
	</h2>
	<button class="bg-orange-500 p-3 rounded-md text-sm text-white mt-4"
		>Contact out sales team
		<i class="fa-regular fa-message ml-2 text-xs"></i></button
	>
	<div class="w-full h-72 md:h-80 lg:h-96 bg-gray-200 mt-8 sm:mt-16 rounded-xl">
		<!-- 빈 박스 -->
	</div>
	<ul class="flex flex-wrap my-20 gap-x-0 gap-y-4 sm:gap-4 justify-between sm:justify-center">
		{#each logos as logo}
			<li class="min-w-24 w-5/12 sm:w-1/6 max-w-52 sm:max-w-28 px-4 sm:px-0 box-border">
				<img src={logo} alt="logo" class="w-full h-full object-scale-down" />
			</li>
		{/each}
	</ul>
</article>
