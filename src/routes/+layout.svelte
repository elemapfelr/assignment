<script>
	import '../app.css';
	import logo from '$lib/assets/slack-logo.svg';

	let menus = [
		{
			title: 'Products',
			link: 'javascript:void(0);'
		},
		{
			title: 'Industries',
			link: 'javascript:void(0);'
		},
		{
			title: 'Resources',
			link: 'javascript:void(0);'
		},
		{
			title: 'Blog',
			link: 'javascript:void(0);'
		}
	];
</script>

<header class="sticky top-0 pt-2.5 bg-white">
	<nav
		class="w-11/12 flex justify-between md:justify-normal mx-auto border-gray-200 border rounded-md shadow-slate-200 shadow-md p-2 items-center bg-white"
	>
		<a href="javascript:void(0);"><img src={logo} alt="logo" /></a>
		<!-- PC -->
		<ul class="hidden md:flex ml-10 gap-8 items-center flex-1">
			{#each menus as menu}
				<li class="text-sm"><a href={menu.link}>{menu.title}</a></li>
			{/each}
		</ul>
		<a href="javascript:void(0);" class="hidden md:inline text-sm mr-10">Login</a>
		<button class="hidden md:inline bg-orange-500 px-2 py-1 rounded-md text-sm text-white"
			>Contact Sales</button
		>
		<!-- mobile -->
		<button class="block md:hidden py-0.5 px-2"><i class="fa-solid fa-bars"></i></button>
	</nav>
</header>

<section class="w-11/12 mx-auto">
	<slot />
</section>
