<section>
	<div>
		<h2>Join Us</h2>
		<ul>
			<li><em>Matins:</em> Sunday at 8:40 a.m.</li>
			<li><em>Divine Liturgy:</em> Sunday at 10:00 a.m.</li>
			<li><em>Vespers:</em> Saturday at 6:00 p.m.</li>
		</ul>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
	}

    div {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		gap: var(--spacing-xl);
		margin: var(--spacing-xxl) var(--spacing-m);
		flex-wrap: wrap;
    }

	@media (max-width: 680px) {
		div {
			flex-direction: column;
			justify-content: flex-start;
			align-items: flex-start;
		}
	}

	h2 {
		font-family: var(--tall-font);
		font-size: var(--font-size-xxl);
		color: var(--color-primary);
        text-transform: uppercase;
	}

	ul {
		min-width: 320px;
        margin-top: -10px;
	}

	em {
		color: var(--color-primary);
	}

	li {
		margin-top: var(--spacing-s);
		font-size: var(--font-size-m);
	}
</style>
