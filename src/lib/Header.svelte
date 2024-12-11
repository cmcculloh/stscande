<div class="banner">
	<p>Sunday Service Hours: Matins @ 8:40am | Divine Liturgy @ 10:00am</p>
</div>
<nav class="navbar">
	<div class="nav-left">
		<div class="nav-item">
			<a href="#">Home</a>
			<div class="dropdown-content">
				<a href="#">Submenu 1</a>
				<a href="#">Submenu 2</a>
			</div>
		</div>
		<div class="nav-item">
			<a href="#">About</a>
			<div class="dropdown-content">
				<a href="#">Submenu 1</a>
				<a href="#">Submenu 2</a>
			</div>
		</div>
		<div class="nav-item">
			<a href="#">Donate</a>
			<div class="dropdown-content">
				<a href="#">Submenu 1</a>
				<a href="#">Submenu 2</a>
			</div>
		</div>
		<div class="nav-item">
			<a href="#">School</a>
			<div class="dropdown-content">
				<a href="#">Submenu 1</a>
				<a href="#">Submenu 2</a>
			</div>
		</div>
		<div class="nav-item">
			<a href="#">Resources</a>
			<div class="dropdown-content">
				<a href="#">Submenu 1</a>
				<a href="#">Submenu 2</a>
			</div>
		</div>
	</div>
	<div class="nav-right">
		<a class="icon social-icon social-icon-youtube" href="https://www.youtube.com/channel/UCHl_paxhbDwNqv2MOZxU2jg" target="_blank">
						<span class="screen-only">Youtube</span>
						<svg class="e-font-icon-svg e-fab-youtube" viewBox="0 0 576 512" xmlns="http://www.w3.org/2000/svg"><path d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z"></path></svg>					</a>
		<input type="text" class="search-box" placeholder="Search..." />
	</div>
</nav>

<style>
	.banner {
		width: 100%;
		height: 40px;
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: var(--color-accent);
		font-family: var(--fine-print-font);
		color: var(--color-secondary);
		font-size: var(--font-size-small);
	}
	.navbar {
		width: 100%;
		height: 100px;
		background-color: var(--color-background);
		display: flex;
		justify-content: space-between;
		align-items: center;
		border-bottom-left-radius: 20px;
		border-bottom-right-radius: 20px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		padding: 0 20px;
		font-family: var(--body-font);

	}
	a {
		text-decoration: none;
		text-transform: uppercase;
		font-weight: var(--font-weight-heavy);
		font-size: 16px;
	}
	.nav-left,
	.nav-right {
		display: flex;
		align-items: center;
	}
	.nav-item {
		margin: 0 10px;
		position: relative;
	}
	.dropdown-content {
		display: none;
		position: absolute;
		background-color: white;
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
		z-index: 1;
	}
	.nav-item:hover .dropdown-content {
		display: block;
	}
	.search-box {
		padding: 5px;
		border: 1px solid #ccc;
		border-radius: 5px;
	}
</style>
