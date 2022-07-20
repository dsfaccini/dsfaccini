<script>
	let today = new Date();
	let birthdate = new Date(1995, 10, 13);
	/**
	 *
	 * @param {Date} start_date
	 * @param {Date} end_date
	 */
	const year_difference = (start_date, end_date = today) =>
		Math.round((end_date.getTime() - start_date.getTime()) / (1000 * 60 * 60 * 24 * 365));
	let moved_to_germany = new Date(2014, 8, 1);
	let time_in_germany = year_difference(moved_to_germany);
	let start_learning_python = new Date(2018, 8, 1);
	let time_learning_to_code = year_difference(start_learning_python);
</script>

<div class="vline" />
<div class="flex flex-col w-6/12 mx-auto mt-5">
	<h2>David Sanchez</h2>
	<hr />
	<p>I code and lift</p>
	<div>
		<p style="display: inline-block;">a little</p>
		<h2 style="display: inline-block;">about me</h2>
	</div>
	<ul>
		<li>born and raised in Bogotá</li>
		<li>moved to Germany {time_in_germany} years ago</li>
		<li>
			Spanish is my native language but I've lived my life in English for as long as I remember
		</li>
		<li>I started started learning to code {time_in_germany} years ago</li>
		<li>I (really) started learning to code {time_learning_to_code} years ago</li>
		<li>I'm CTO at <a href="/emprendeseo">Emprende-SEO</a></li>
		<li>and software developer at Brettschneider</li>
	</ul>
	<h2>about my skills</h2>
	<small>
		<details>
			<summary>summary of things I've learnt coding</summary>
			<details>
				<summary> python </summary>
				<ul>
					<li>
						<p>pandas</p>
						<p>plotly</p>
						<p>seaborn</p>
						<p>statsmodels</p>
					</li>
				</ul>
			</details>
		</details>
	</small>
	<section>
		<h3>programming languages and not programming languages, sorted by proficiency</h3>
		<ol>
			<li>python</li>
			<li>sql</li>
			<li>javascript</li>
			<li>html</li>
			<li>css</li>
			<li>bash</li>
			<li>batch</li>
		</ol>
		<h3>frontend stack</h3>
		<ul>
			<li>sveltekit for all my projects (cause it comes with a handy backend)</li>
			<li>if I only need the client I make a static build</li>
			<li>
				I tried out
				<a href="/react"> react, </a>
				I just like svelte a lot more
			</li>

			<li>tailwind to spare me some style tags</li>
			<li>flexbox and grid both, dunno what the controversy's all about</li>
		</ul>
		<h3>backend stack</h3>
		<ul>
			<li>svelte<i>kit</i> as mentioned above</li>
			<li>
				strapi for the simplicity of defining content types and the aesthetic for the end &ndash;
				admin &ndash; user
			</li>
			<li>django</li>
			<li>flask</li>
			<li>postgres</li>
		</ul>
	</section>
</div>

<style>
	summary {
		cursor: pointer;
	}
	h3 {
		/* border-top: 1px solid rgba(0, 0, 0, 0.493); */
		margin: 5px 0 10px 0;
		border-bottom: 1px solid grey;
	}
	.vline {
		display: none;
		position: absolute;
		background-color: blue;
		width: 3px;
		height: 100vh;
		left: 26%;
	}
	ul li::before {
		content: '~';
		color: var(--ouryellow);
		margin-right: 10px;
	}
	ul,
	ol {
		margin-left: 5px;
	}
	ol {
		counter-reset: counter-name;
	}
	ol li::before {
		counter-increment: counter-name;
		content: counter(counter-name);
		color: var(--ouryellow);
		margin-right: 12px;
		cursor: pointer;
		transition: all ease-in-out 400ms;
	}
	ol li:hover {
		cursor: pointer;
	}
	ol li:hover::before {
		counter-increment: counter-name;
		content: counter(counter-name) ' ->';
		color: var(--ouryellow);
		margin-right: 15px;
		/* transition: margin ease 300ms; */
	}
</style>
