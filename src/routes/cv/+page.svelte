<script lang="ts">
	import pp from '$lib/cv-components/me-atlantis-30.jpg';
	import Email from '$lib/icons/Email.svelte';
	import GeoAlt from '$lib/icons/GeoAlt.svelte';
	import Linkedin from '$lib/icons/Linkedin.svelte';
	import Pagebreak from '$lib/utility-components/Pagebreak.svelte';
	import ExperienceCard from '$lib/cv-components/ExperienceCard.svelte';

	// https://stackoverflow.com/questions/4782068/can-i-set-subject-content-of-email-using-mailto
	let email_linebreak = '%0D%0A';
	let email_body = `Hey David${email_linebreak}${email_linebreak}I stumbled upon Your CV and think You'd fit very well one of the positions I'm recruiting for${email_linebreak}The title of the position is Title, You'd be responsible for tasks a, b, c and d among others${email_linebreak}The company has an office in Location and their budget for this position ranges from x to y${email_linebreak}Could we arrange a call say on Monday around 2PM to discuss it?${email_linebreak}${email_linebreak}Best regards`;
	let email_href = `mailto:dsfapps+cv@gmail.com?subject=Career Opportunity&body=${email_body}`;
	let linkedin_href = 'https://linkedin.com/in/david-s-a88114140';
</script>

<svelte:head>
	<title>CV David SF</title>
</svelte:head>
<div class="outer">
	<header>
		<div>
			<h1 class="text-4xl font-bold">David Sánchez Faccini</h1>
			<p class="text-xl">Data Engineer</p>
			<p class="text-sm text-center mt-2 gradient-text">python - sql - linux - docker - aws</p>
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
		<div class="skills-description bottom-line">
			<img src={pp} alt="hertz" />
			<section class="description my-auto font-medium">
				<li>Data is key to making good decisions</li>
				<li>We won't use data if it's not readily available</li>
				<li>We should simplify behaviors we want to promote</li>
				<li style="list-style: none; margin-top: 2px; font-size: 1.1em;">
					My mission is to facilitate answers to the right questions, using data
				</li>
			</section>
		</div>
		<main>
			<section class="experiences">
				<h2>Experiences</h2>
				<div class="flex flex-col gap-4 mt-2">
					<ExperienceCard title="Data engineer" place="atlantis dx" date_range="Mar 2023 - present">
						<li>
							atlantis is an agency facilitating companies' digitalization efforts. Our clients are
							mainly B2B companies from the german SME.
						</li>
						<li>
							In our data & analytics area I train our Azubis and support our clients on their ETL-,
							data warehouse- and middleware projects.
						</li>
						<li>
							In the company I'm in charge of our own data warehouse and work across departments
							advising on interdisciplinary projects, specially around APIs and process automation.
						</li>
						<li>
							I also stay on top of the latest LLM developments and integrate them into our sales
							processes and POCs
						</li>
					</ExperienceCard>
					<ExperienceCard
						title="Software developer"
						place="Brettschneider"
						date_range="Jun 2022 - Feb 2023"
					>
						<p>
							Brettschneider is a logistics provider. Here I was tasked with automating processes.
						</p>
						<p>
							Our operations were based on MSSQL and our logistics software, I created a python
							codebase for the new services:
						</p>
						<li>
							Automating invoicing - saving management and accounting up to a week of work every
							month
						</li>
						<li>
							Automating weekly reports to our clients - saving our customer support hours in weekly
							manual tasks and improving our CX
						</li>
						<li>
							Building event-driven systems and integrating provider APIs - allowing us to package
							and ship twice as many collis and saving hours in daily operations
						</li>
					</ExperienceCard>
					<Pagebreak />
					<ExperienceCard
						title="Data analyst"
						place="Design Bestseller"
						date_range="Oct 2019 - May 2022"
					>
						<p>DBS is an e-commerce company selling designer furniture.</p>
						<p>My work there was very varied:</p>
						<li>Automating weekly and monthly reports using our exasol data warehouse</li>
						<li>
							Creating new reports in Power BI and engineering potential features to be used as KPIs
							<div>
								<li>
									for instance, displaying our highest impact products on a dashboard to increase
									average order value
								</li>
							</div>
						</li>
						<li>Scraping external data sources to improve our customer experience</li>
						<p>
							Building models:
							<li>A market basket analysis model to power a potential recommendation engine</li>
							<li>A customer lifetime value model to better measure our marketing budget</li>
							<li>
								A time series model to predict the availability of products and improve purchasing
								and inventory
							</li>
						</p>
					</ExperienceCard>
					<ExperienceCard title="Tech lead" place="Emprende-SEO" date_range="Feb 2021 - Feb 2023">
						<p>Emprende-SEO was an enterprise partly owned by me.</p>
						<p>There I was responsible for:</p>
						<li>Advising our clients on technical solutions</li>
						<li>Building applications, such as booking systems or serverless functions</li>
						<li>Automating processes</li>
						<li>Integrating external APIs</li>
					</ExperienceCard>
					<ExperienceCard
						title="Working student"
						place="Institute of ferrous metals at RWTH Aachen"
						date_range="Nov 2018 - Mar 2021"
					>
						<p>I was making simulations of elasticity models of steel.</p>
						<p>The progress was very slow because getting the data I needed took several weeks.</p>
						<p>I automated the steps — and got the time down to minutes — for the process of:</p>
						<li>preparing the experimental data to be used in the models</li>
						<li>evaluating the simulation results</li>
						<p>
							I also automated the process of iterating over model parameters between simulations,
							to find optimal parameters and eliminating the need for human supervision during
							long-running, compute-intensive simulations
						</p>
					</ExperienceCard>
				</div>
			</section>
			<section class="certificates">
				<h2>Certificates</h2>
				<ul>
					<li>
						(IBM)
						<a href="https://www.credly.com/badges/d2cbd3a7-d933-4432-8f30-0faca1444d37/public_url"
							>Applied Data Science with Python</a
						>
					</li>
					<li>
						(DataCamp)
						<a href="https://www.datacamp.com/skill-verification/DL0028270650070">Data Literacy</a>
					</li>
					<li>
						(Coursera)
						<a
							href="https://www.coursera.org/account/accomplishments/specialization/certificate/BNLZMBY84NGY"
							>Biostatistics in Public Health</a
						>
					</li>
					<li>
						(LinkedIn)
						<a
							href="https://www.linkedin.com/learning/certificates/5d16f86c30bb49a96afba7b1b6854be847c388c803ef2289551368004928374b"
							>Decision Intelligence</a
						>
					</li>
				</ul>
			</section>
		</main>
	</div>
</div>

<style>
	.gradient-text {
		background: linear-gradient(90deg, green, rgb(175, 175, 0), orange);
		background-clip: text;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	img {
		border-radius: 1em;
	}
	.outer {
		max-width: 1000px;
		margin: 10px auto;
		/* background: linear-gradient(135deg, rgba(148, 148, 148, 0.374), rgba(119, 136, 153, 0.8)); */
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
		border-bottom: 2px solid black;
		padding-bottom: 10px;
	}
	li {
		list-style: inherit;
		margin-left: 25px;
	}

	ul {
		list-style: circle;
	}
	h2 {
		width: 80%;
		padding: 10px 0;
		font-size: 20px;
		font-weight: bold;
	}

	header {
		display: grid;
		grid-template-columns: 60% 40%;
		text-align: center;
		margin: 20px auto;
	}

	.skills-description {
		display: grid;
		margin: 0 auto;
		grid-template-columns: 24% 76%;
	}
	header ul li {
		display: grid;
		grid-template-columns: 10% 90%;
		align-items: center;
		text-align: left;
	}
</style>
