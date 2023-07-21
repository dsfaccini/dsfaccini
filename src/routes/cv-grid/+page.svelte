<script>
	import pp from '$lib/cv-components/pp.jpg';
	import Email from '$lib/icons/Email.svelte';
	import GeoAlt from '$lib/icons/GeoAlt.svelte';
	import Linkedin from '$lib/icons/Linkedin.svelte';
	import ExperienceCard from '$lib/cv-components/ExperienceCard.svelte';

	// https://stackoverflow.com/questions/4782068/can-i-set-subject-content-of-email-using-mailto
	let email_linebreak = '%0D%0A';
	let email_body = `Hey David${email_linebreak}${email_linebreak}I stumbled upon Your CV and think You'd fit very well one of the positions I'm recruiting for${email_linebreak}The title of the position is Title, You'd be responsible for tasks a, b, c and d among others${email_linebreak}The company has an office in Location and their budget for this position ranges from x to y${email_linebreak}Could we arrange a call say on Monday around 2PM to discuss it?${email_linebreak}${email_linebreak}Best regards`;
	let email_href = `mailto:dsfapps@gmail.com?subject=Career Opportunity&body=${email_body}`;
	let linkedin_href = 'https://linkedin.com/in/david-s-a88114140';
</script>

<svelte:head>
	<title>CV David SF</title>
</svelte:head>
<div class="outer">
	<header>
		<div>
			<h1 class="text-4xl font-bold">David Sánchez Faccini</h1>
			<p class="text-xl">Software Developer</p>
		</div>
		<ul>
			<li>
				<a href={linkedin_href}><Linkedin /></a>
				<a href={linkedin_href}>linkedin.com/in/david-s-a88114140</a>
			</li>
			<li>
				<a href={email_href}>
					<Email />
				</a>
				<a href={email_href}>dsfapps&#64;gmail&#46;com</a>
			</li>
			<li>
				<GeoAlt />
				Hamburg, Germany
			</li>
		</ul>
	</header>
	<div>
		<div class="bottom-line" style="display: grid; grid-template-columns: 15% 2% 10% 2% 71%">
			<img src={pp} alt="hertz" />
			<hr class="vertical" />
			<div class="skills">
				<!--p>python - sql - typescript - shell - docker</p-->
				<ul class="text-left">
					<li>python</li>
					<li>sql</li>
					<li>typescript</li>
					<li>shell</li>
					<li>docker</li>
				</ul>
			</div>
			<hr class="vertical" />
			<section class="description my-auto font-medium">
				<li>I believe data is key to making good decisions</li>
				<li>People won't use data if it's not easy to access and understand</li>
				<li>We should facilitate behaviors we want to promote</li>
				<li>
					That's why I like building tools that people like to use and make their lives easier
				</li>
				<li>Data today isn't only bytes, it's Software</li>
			</section>
		</div>
		<main>
			<section class="experiences">
				<h2>Experiences</h2>
				<div class="flex flex-col-reverse gap-4 mt-2">
					<ExperienceCard
						title="Working student"
						place="Institute of ferrous metals at RWTH Aachen"
						date_range="Nov 2018 - Mar 2021"
					>
						<p>
							I was making simulations of elasticity models of steel<br />
							The progress was very slow because getting the data I needed took several weeks <br />
							I automated the steps and got the time down to minutes for the process of
						</p>
						<li>preparing the experimental data to be used in the models</li>
						<li>evaluating the simulation results</li>
						<p>
							I also automated the process of iterating over model parameters between simulations,
							to find optimal parameters and eliminating the need for human supervision during
							long-running, compute-intensive simulations
						</p>
					</ExperienceCard>
					<ExperienceCard
						title="Data analyst"
						place="Design Bestseller"
						date_range="Oct 2019 - May 2022"
					>
						<p>
							The work was very varied
							<li>automating weekly and monthly reports using our exasol data warehouse</li>
							<li>
								creating new reports and engineering features that could be used as KPIs
								<div>
									<li>
										like a dashboard to display our highest impact products to increase average
										order value
									</li>
								</div>
							</li>
							<li>scraping external data sources to improve our customer experience</li>
						</p>
						<p>
							I built a couple of models that I sadly didn't get to see through to production
							<li>A market basket analysis model to power a potential recommendation engine</li>
							<li>A customer lifetime value model to better measure our marketing budget</li>
							<li>
								A time series model to predict the availability of products and improve purchasing
								and inventory
							</li>
						</p>
					</ExperienceCard>
					<ExperienceCard title="Tech lead" place="Emprende-SEO" date_range="Feb 2021 - Mar 2023">
						<p>
							Emprende-SEO was an enterprise partly owned by me
							<br />
							There I was responsible for:
						</p>
						<li>advising our clients on potential technical solutions</li>
						<li>building applications (like booking systems or APIs)</li>
						<li>automating processes</li>
						<li>integrating external APIs</li>
					</ExperienceCard>
					<ExperienceCard
						title="Software developer"
						place="Brettschneider"
						date_range="Mai 2022 - Mar 2023"
					>
						<p>
							Work at Brettschneider was great, I was tasked with automating processes and had a lot
							of autonomy
						</p>
						<p>
							Our operations were based on MSSQL and our logistics software, I created a python
							codebase for the new services
						</p>
						<li>
							Automating invoices - saved management and accounting a couple of days of work every
							month
						</li>
						<li>Automating weekly reports to our clients - saved a couple of hours every week</li>
						<li>
							Building event-driven systems and integrating provider APIs - allowed us to package
							and ship twice as many collis and save hours in daily operations
						</li>
					</ExperienceCard>
				</div>
			</section>
		</main>
	</div>
</div>

<style>
	.outer {
		max-width: 1000px;
		margin: 10px auto;
		background: linear-gradient(135deg, rgba(148, 148, 148, 0.374), rgba(119, 136, 153, 0.8));
		border-radius: 1em;
		padding: 10px 20px;
	}
	a {
		/*
		diagonal linear gradient light blue with a tip of orange
		background: linear-gradient(to bottom right, #add8e6, #add8e6 90%, #ffa500 10%);
		*/
		color: cornflowerblue;
	}
	.bottom-line {
		border-bottom: 3px solid black;
		padding-bottom: 10px;
	}
	li {
		list-style: circle;
		margin-left: 25px;
	}
	h2 {
		width: 80%;
		padding: 10px 0;
		font-size: 20px;
		font-weight: bold;
	}
	hr.vertical {
		width: 3px;
		margin: 5px;
		height: 100%;
		background-color: black;
	}
	header {
		display: grid;
		grid-template-columns: 60% 40%;
		text-align: center;
		margin: 20px auto;
	}
	header ul li {
		display: grid;
		grid-template-columns: 10% 90%;
		align-items: center;
		text-align: left;
	}
</style>
