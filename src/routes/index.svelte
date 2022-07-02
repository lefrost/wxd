<script lang="ts">
	let links = [
		{
			id: `instagram`,
			text: `Instagram`,
			url: `https://www.instagram.com/travisliaw`
		},
		{
			id: `twitter`,
			text: `Twitter`,
			url: `https://twitter.com/wxd_nft`
		},
		{
			id: `suaveseals`,
			text: `Suave Seals`,
			url: `https://www.suaveseals.com/profile/wxd`
		}
	];
</script>

<div class="container  grow--  col--  col-centre--  landing">
	<div class="landing-heading">wxd</div>

	<div class="container  col--  landing-main">
		<div class="container  col--  col-centre--  row-md--">
			<div class="container  landing-main__heading">
				<span>
					sup<br />bitch
				</span>
				<div />
			</div>

			<img src="./images/image.png" alt="" class="landing-main__image" />
		</div>

		<div class="container  row--  landing-main__bio">
			<div class="container  stretch--" />
			<div>
				Trav here, a Community Manager and huge Degen influenced by
				<a href="https://twitter.com/lefrst" target="_blank"> @lefrost </a>
				and
				<a href="https://twitter.com/cdercer" target="_blank"> @crsy </a>
				and based in ur mom's room.
			</div>
		</div>

		<div class="container  row--  row-wrap--  landing-main__links">
			{#each links as link}
				<a href={link.url} target="_blank" class="landing-main__link">
					{link.text}
				</a>
			{/each}
		</div>
	</div>
</div>

<style lang="scss">
	@import '../assets/scss/all.scss';

	.landing {
		width: calc(100% - $wrapper-gutter * 2);
		max-width: 1500px;
	}

	.landing-heading {
		color: $purple;
		font-size: 1.2em;
		padding: 1em;
	}

	.landing-main {
		padding: 4em 0;
		font-size: 0.7em;
		align-items: center !important;

		@media (min-width: $bp-md) {
			font-size: 1em;
			align-items: flex-start !important;
		}
	}

	.landing-main__heading {
		position: relative;

		> span {
			text-transform: uppercase;
			font-size: 4em;
			letter-spacing: 0.03em;
			z-index: 1;
		}

		> div {
			position: absolute;
			background-color: rgba($purple, 0.3);
			width: 20em;
			height: 2.4em;
			bottom: 0em;
			left: 2em;
			z-index: 0;
		}
	}

	.landing-main__image {
		width: 7em;
		height: 7em;
		border: 0.4em solid $purple;
		border-radius: 50%;
		margin: 2em 0;

		@media (min-width: $bp-md) {
			width: 14em;
			height: 14em;
			margin: 0;
			margin-left: 3em;
		}
	}

	.landing-main__bio {
		padding-top: 2em;

		> div {
			&:nth-of-type(1) {
				width: 0.6em;
				background-color: rgba($purple, 0.3);
				margin-right: 1.5em;
			}

			&:nth-of-type(2) {
				max-width: 36em;
				font-size: 0.9em;
				line-height: 1.3em;

				> a {
					text-decoration: underline;
					color: rgba($purple, 0.7);
					@include swish;

					&:hover {
						color: $purple;
					}
				}
			}
		}
	}

	.landing-main__links {
		padding-top: 2em;
	}

	.landing-main__link {
		border: 0.15em solid $purple;
		padding: 0.5em 1em;
		color: $purple;
		font-size: 0.7em;
		@include swish;

		&:hover {
			background-color: $purple;
			color: $white;
		}

		&:not(:first-of-type) {
			margin-left: 0.8em;
		}
	}
</style>
