<script>
	import censor from '/assets/censor.gif';
	import picture from '/assets/picture.png';
	import blahaj from '/assets/blahaj.png'
	import { page } from '$app/stores';
</script>

<svelte:head>
	<title>{$page.url.pathname} | charlie's webcave</title>
	<meta content="#FFC0CB" data-react-helmet="true" name="theme-color" />
	<meta property="og:title" content="charlie's house in the interwebs | {$page.url.pathname}" />
	<meta property="og:description" content="yeah uh this charlie nest of autism" />
	<meta property="og:url" content="https://t480.dev{$page.url.pathname}" />
	<meta property="og:image" content={picture} />
	<a rel="me" href="https://hachyderm.io/@imcharlie">Mastodon</a>
</svelte:head>

<header>
	<h1>charlie's webcave</h1>
	<p>you know youre better than this.</p>
</header>

<main>
	<nav>
		<div class="links">
			<a href="/" class:active={$page.url.pathname == '/'}><i class="fa-solid fa-house"></i> home</a>
			<a href="/blog/" class:active={$page.url.pathname == '/blog/'}><i class="fa-solid fa-newspaper"></i> my blog</a>
			<a href="/about" class:active={$page.url.pathname == '/about/'}><i class="fa-solid fa-address-card"></i> about me</a>
			<a href="/projects" class:active={$page.url.pathname == '/projects/'}><i class="fa-solid fa-code"></i> projects</a>
			<a href="/resources" class:active={$page.url.pathname == '/resources/'}><i class="fa-solid fa-folder"></i> resources</a>
			<a href="/contact" class:active={$page.url.pathname == '/contact/'}><i class="fa-solid fa-paper-plane"></i> contact</a>
			<a href="/presence" class:active={$page.url.pathname == '/presence/'}><i class="fa-solid fa-user"></i> presence</a>
			<a href="/donate" class:active={$page.url.pathname == '/donate/'}><i class="fa-solid fa-piggy-bank"></i> donate</a>
		</div>
		<div class="images">
			<hr />
			<img src={picture} alt="blahaj." title="me.png" id="picture" />
			<hr />
			<a href="https://www.mabsland.com/Adoption.html" id="censor"><img src={censor} alt="website content is rated WEB-14" title="This site is rated WEB-14. However, external links may not be rated." /></a>
		</div>
	</nav>

	<article>
		<slot />
	</article>
</main>

<footer>
	<p><i>made with</i> ❤ <i>by charlie | <i>site last modified may 19th 2025</i> | <a href="https://github.com/a53xd/www">source code viewable here</a></i></p>
	<p><img src="{blahaj}" style="height:15px;"> certified Good Website by blåhaj</p>
</footer>
