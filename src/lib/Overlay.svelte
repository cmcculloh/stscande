<script lang="ts">
	let { heading, links } = $props();
</script>

<section class="overlay">
	<div class="content">
		<h1>{heading}</h1>
		<div class="buttons">
			{#each links as link, index}
				<a class={index === 0 ? 'button accent' : 'button alternate'} href={link.href}>
					{link.text}
					{#if link.href.startsWith('http')}
						<svg aria-hidden="true" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg">
							<path
								d="M432,320H400a16,16,0,0,0-16,16V448H64V128H208a16,16,0,0,0,16-16V80a16,16,0,0,0-16-16H48A48,48,0,0,0,0,112V464a48,48,0,0,0,48,48H400a48,48,0,0,0,48-48V336A16,16,0,0,0,432,320ZM488,0h-128c-21.37,0-32.05,25.91-17,41l35.73,35.73L135,320.37a24,24,0,0,0,0,34L157.67,377a24,24,0,0,0,34,0L435.28,133.32,471,169c15,15,41,4.5,41-17V24A24,24,0,0,0,488,0Z"
							></path>
						</svg>
					{/if}
				</a>
			{/each}
		</div>
	</div>
</section>

<style>
	.overlay {
		margin-top: calc(-1 * var(--spacing-m));
		position: relative;
		width: 100%;
		height: 90vh;
		overflow: hidden;
		background-image: url('/img/home-banner.jpg');
		background-size: cover;
		background-position: center;
		z-index: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 0 0 var(--border-radius-l) var(--border-radius-l);
	}

	.content {
		display: flex;
		justify-content: flex-end;
		align-content: flex-end;
		align-items: center;
		width: 100%;
		padding: var(--spacing-m);
		box-sizing: border-box;
        flex-wrap: wrap;
	}

    .buttons {
		display: flex;
		gap: var(--spacing-l);
		align-self: flex-start;
        padding-top: var(--spacing-l);

	}

	h1 {
		text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
	}

	h1, .buttons {
		width: 90%;
	}

	.buttons {
		flex-direction: row;
        flex-wrap: wrap;
	}

	@media (min-width: 1300px) {
		h1 {
			width: 63%;
		}

        .buttons {
            width: 37%;
            justify-content: center;
        }
	}
</style>
