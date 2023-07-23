<script>
	import Centered from '$lib/containers/Centered.svelte';
	import BlockQuote from '$lib/containers/BlockQuote.svelte';
	import Pagebreak from '$lib/utility-components/Pagebreak.svelte';
	import BlackCenteredText from '$lib/containers/BlackCenteredText.svelte';
	// https://www.linkedin.com/pulse/ultimate-linkedin-post-type-guide-peter-lowes/
	let video_href = 'https://www.youtube.com/watch?v=ND_AjF_KTD8';
</script>

<svelte:head>
	<title>LinkedIn</title>
</svelte:head>

<Centered>
	<h1>
		<a href={video_href}> The next decade of SWD 2023 </a>
	</h1>
	<p>
		I stumbled upon this talk from the NDC London 2023 and wanted to share some of the more
		interesting points he makes about the present and next couple of years
	</p>
	<Pagebreak />
	<div class="flex flex-row justify-between">
		<h2>The shifting importance of growth to ROI in a tight economic climate</h2>
		<a href="{video_href}?t=1345">minute 22:25</a>
	</div>
	<BlackCenteredText>
		<BlockQuote>
			Software developers are rarely responsible to make money for the company [...] it's in our
			best interest with our skills and domain knowledge to:

			<li>make sure you know how your company makes money</li>
			<li>make sure the things you're building help that</li>
			<p>
				Because we are productivity amplifiers, we're incredibly good at building tools that allow
				the rest to work faster, to do more
			</p>
			<p>We can help companies survive in difficult times if we work on the right things</p>
		</BlockQuote>
	</BlackCenteredText>
	<Pagebreak />
	<div class="flex flex-row justify-between">
		<h2>Cyber security and containers</h2>
		<a href="{video_href}?t=2375">minute 39:35</a>
	</div>
	<BlackCenteredText>
		<BlockQuote>
			I look at what's happened in cyber insurance in the past couple of years
			<p>
				today if you want to get Cyber Insurance not only is it more expensive but they require
				multi-factor authentication
			</p>
			<p>more and more I'm seeing things like, you're required to do a privileged access audit</p>
			<p>
				it wouldn't surprise me at all if the insurers at some point say: "if your apps aren't
				running containers you're not insured"
			</p>
		</BlockQuote>
	</BlackCenteredText>
</Centered>

<style>
	p:first-letter {
		text-transform: capitalize;
	}
	h2 + a {
		font-size: 0.9em;
		font-style: italic;
	}
	h2 {
		font-size: 1.5rem;
		font-weight: bold;
		line-height: 1.2;
		margin-bottom: 1rem;
	}
	h1 {
		font-size: 2rem;
		font-weight: bold;
		line-height: 1.2;
		margin-bottom: 1rem;
	}
</style>
