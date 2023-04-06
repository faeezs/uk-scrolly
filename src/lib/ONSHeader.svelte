<script>
	import { themes } from '../config.js';
	import { getContext } from 'svelte';

	export let theme = getContext('theme');
</script>

<footer style="color: {themes[theme]['text']}; background-color: {themes[theme]['pale']};">
	<div class="col-wide" data-analytics="footer">
		<a href="https://www.ons.gov.uk/">
			{#if theme == 'dark'}
			<img
				class="logo-img"
				src="./img/ons-logo-neg-en.svg"
				alt="Office for National Statistics" />
			{:else}
			<img
				class="logo-img"
				src="./img/ons-logo-black-en.svg"
				alt="Office for National Statistics" />
			{/if}
		</a>
		<ul>
			<li><a href="https://www.ons.gov.uk/aboutus/contactus" class="link" style="color: {themes[theme]['text']}">Contact us</a></li>
			<li><a href="https://www.ons.gov.uk/help/privacynotice" class="link" style="color: {themes[theme]['text']}">Cookies and privacy</a></li>
		</ul>
	</div>
</footer>

<style>
	footer {
		padding-bottom: 72px;
		padding-top: 36px;
		font-size: 18px;
	}
	footer a.link {
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		text-decoration: underline;
		display: inline-block;
	}
	footer a.link:hover {
		text-decoration: none;
	}
	footer a.link:active {
		outline: 3px solid transparent;
		background-color: #fd0;
		-webkit-box-shadow: 0 -2px #fd0, 0 4px #222;
		box-shadow: 0 -2px #fd0, 0 4px #222;
		color: #222;
		text-decoration: none;
	}
	ul {
		padding: 0;
		margin: 0;
	}
	li {
		margin-right: 18px;
		display: inline-block;
	}
	.logo-img {
		margin-bottom: 27px;
	}
	a img:hover {
		cursor: pointer;
	}
</style>