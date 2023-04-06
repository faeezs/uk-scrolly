<script>
	import { themes } from '../config.js';
	import { getContext } from 'svelte';

	export let theme = getContext('theme');
</script>

<footer style="--text: {themes[theme]['text']}; --muted: {themes[theme]['muted']}; --pale: {themes[theme]['pale']};">
	<div class="col-wide" data-analytics="footer">
		
		<div class="license">
			All content is available under the
			<a
				href="https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/"
				class="external-link"
				target="_blank"
				rel="noopener">Open Government Licence v3.0</a>, 
			except where otherwise stated
		</div>
	</div>
</footer>

<style>
	footer {
		color: var(--text);
		background-color: var(--pale);
		padding-bottom: 72px;
		padding-top: 36px;
		font-size: 18px;
	}
	footer a {
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		color: var(--muted);
		text-decoration: underline;
		display: inline-block;
	}
	footer a:hover {
		color: var(--text);
		text-decoration: none;
	}
	footer a:active {
		outline: 3px solid transparent;
		background-color: #fd0;
		-webkit-box-shadow: 0 -2px #fd0, 0 4px #222;
		box-shadow: 0 -2px #fd0, 0 4px #222;
		color: #222;
		text-decoration: none;
	}
	.license {
		vertical-align: top;
	}
</style>