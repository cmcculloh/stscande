<script lang="ts">
	import { page } from '$app/stores';
	const menus = [
		{
			item: { name: 'Home', href: '/' }
		},
		{
			item: { name: 'About', href: '/about' },
			menuItems: [
				{ name: 'Contact', href: '/about/contact' },
				{ name: 'Leadership', href: '/about/leadership' },
				{ name: 'Youth', href: '/about/youth' },
				{ name: 'Music', href: '/about/music' }
			]
		},
		{
			item: { name: 'Donate', href: '/donate' }
		},
		{
			item: { name: 'School', href: '/school' }
		},
		{
			item: { name: 'Resources', href: '/resources' },
			menuItems: [
				{ name: 'Parish Directory 🔒', href: '/resources/parish-directory' },
				{
					name: 'Monthly Calendar',
					href: 'https://www.google.com/calendar/embed?title=Calendar&amp;showTz=0&amp;height=600&amp;wkst=1&amp;bgcolor=%23ffffff&amp;src=dbb89q1e39rpomrlk7v8l5k2ug%40group.calendar.google.com&amp;color=%232952A3&amp;ctz=America%2FNew_York'
				},
				{ name: 'Streaming', href: 'https://www.youtube.com/channel/UCHl_paxhbDwNqv2MOZxU2jg' },
				{ name: 'Readings', href: 'https://oca.org/readings' },
				{ name: 'Tipic', href: 'https://roea.org/calendartipicpaschalia' },
				{ name: 'Episcopate', href: 'https://roea.org/' }
			]
		}
	];

	const isActive = (path: string) => {
		if (path === '/') {
			return $page.url.pathname === '/';
		}
		return $page.url.pathname.startsWith(path);
	};
</script>

{#each menus as menu}
	<li class="nav-item">
		<a class={isActive(menu.item.href) ? 'active' : ''} href={menu.item.href}>{menu.item.name}</a>
		{#if menu.menuItems}
			<ul class="dropdown-content">
				{#each menu.menuItems as item}
					<li>
						<a class={isActive(item.href) ? 'active' : ''} href={item.href}
							>{item.name}
							{#if item.href.startsWith('http')}
								➡︎{/if}</a
						>
					</li>
				{/each}
			</ul>
		{/if}
	</li>
{/each}

<style>
	a {
		text-decoration: none;
		text-transform: uppercase;
		font-weight: var(--font-weight-heavy);
		font-size: 16px;
	}
	.nav-item {
		list-style: none;
		position: relative;
		display: flex;
		flex-direction: column;
		margin: 0 10px;
		box-sizing: border-box;
		vertical-align: baseline;
	}
	.dropdown-content {
		visibility: hidden;
		opacity: 0;
		position: absolute;
		background-color: white;
		z-index: 1;
		margin-top: 0px;
		padding: 0px 30px 30px;
		border-radius: 0 0 var(--border-radius-s) var(--border-radius-s);
		min-width: 200px;
		top: 100%;
		z-index: 99999;
		left: -20px;
		border-bottom: 1px solid #eee;
		transition:
			visibility 0.3s ease-in-out,
			opacity 0.3s ease-in-out;
		box-shadow: 0 1px 0px rgba(0, 0, 0, 0.1);
	}

	.dropdown-content li {
		margin-top: 20px;
		list-style: none;
	}

	.nav-item:hover .dropdown-content,
	.nav-item:focus-within .dropdown-content {
		opacity: 1;
		visibility: visible;
	}
</style>
