<script>
	import '../app.css';
	import logo from '$lib/assets/slack-logo.svg';

	let menus = [
		{
			title: 'Products',
			link: '/Products'
		},
		{
			title: 'Industries',
			link: '/Industries'
		},
		{
			title: 'Resources',
			link: '/Resources'
		},
		{
			title: 'Blog',
			link: '/Blog'
		}
	];
</script>

<nav
	class="sticky top-2.5 w-11/12 flex mt-2.5 mx-auto border-gray-200 border rounded-md shadow-slate-200 shadow-md p-2 items-center bg-white"
>
	<a href="/"><img src={logo} alt="logo" /></a>
	<ul class="flex ml-10 gap-8 items-center flex-1">
		{#each menus as menu}
			<li class="text-sm"><a href={menu.link}>{menu.title}</a></li>
		{/each}
	</ul>
	<a href="/Login" class="text-sm mr-10">Login</a>
	<button class="bg-orange-500 px-2 py-1 rounded-md text-sm text-white">Contact Sales</button>
</nav>
<section class="w-11/12 mx-auto">
	<slot />
</section>
