<script lang="ts">
	/**
	 * The url to share
	 */
	export let url: string;

	/**
	 * Accessibility label that will be shown on the parent <a> tag.
	 */
	export let ariaLabel = 'Share on Social Media';

	/**
	 * Whether to display the icon
	 */
	export let showIcon = true;

	let classes = '';

	export { classes as class };
</script>

<a
	class="share-button__link"
	href={url}
	target="_black"
	rel="noopener noreferrer"
	aria-label={ariaLabel}
>
	<div class="share-button__button {classes}">
		{#if showIcon}
			<div class="share-button__icon" aria-hidden="true">
				<slot name="icon" />
			</div>
		{/if}
		<slot />
	</div>
</a>

<style>
	.share-button__link {
		display: var(--share-link-display, inline-block);
		text-decoration: var(--share-link-text-decoration, none);
		color: var(--share-link-color, #fff);

		cursor: pointer;
	}

	.share-button__button {
		display: flex;
		flex-direction: row;
		justify-content: var(--share-button-justify-content, space-between);
		align-items: center;

		gap: var(--share-button-gap, 0.5em);

		padding: var(--share-padding, 0.75em);
		background-color: var(--share-button-background-color, #000);
	}

	.share-button__button:active,
	.share-button__button:hover {
		background-color: var(--share-button-hover-color, #000);
	}

	:global(.share-button__icon svg) {
		margin: 0;
		padding: 0;
		vertical-align: middle;
	}
</style>
