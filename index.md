---
layout: home
title: Goffar.com
---

## Welcome to Goffar.com

A collection of projects, demos, and experiments. Click any project below to learn more and try it out.

---

## Projects

<div class="project-filters" aria-label="Filter projects by technology">
	<button class="filter-btn active" type="button" data-filter="all">All</button>
	<button class="filter-btn" type="button" data-filter="ASP.NET">ASP.NET</button>
	<button class="filter-btn" type="button" data-filter="Blazor">Blazor</button>
	<button class="filter-btn" type="button" data-filter="Razor Pages">Razor Pages</button>
	<button class="filter-btn" type="button" data-filter="SQL Server">SQL Server</button>
	<button class="filter-btn" type="button" data-filter="Azure App Service">Azure App Service</button>
	<button class="filter-btn" type="button" data-filter="OpenAI API">OpenAI API</button>
</div>

<p class="filter-status" id="filter-status">Showing all projects.</p>

<div class="project-grid" id="project-grid">
	<article class="project-card" data-tech="ASP.NET|Razor Pages|Blazor|SQL Server|Azure App Service|OpenAI API">
		<h3>🗺️ BiblePaths.NET</h3>
		<p>Bible Paths is a full stack crowd sourced Bible study and devotional tool. Each Bible Path is a chain of Bible verses linked together to form a simple, self contained Bible study.</p>
		<div class="tech-pills" aria-label="BiblePaths technologies">
			<button class="tech-pill tech-pill-link" type="button" data-filter="ASP.NET">ASP.NET</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="Razor Pages">Razor Pages</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="Blazor">Blazor</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="SQL Server">SQL Server</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="Azure App Service">Azure App Service</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="OpenAI API">OpenAI API</button>
		</div>
		<p><a href="/BiblePaths/">View Project →</a></p>
	</article>

	<article class="project-card" data-tech="ASP.NET|Blazor|SQL Server|Azure App Service">
		<h3>🗺️ BiblePaths.NET/PBE</h3>
		<p>Powered by BiblePaths.Net, the Pathfinder Bible Experience (PBE) quiz app is designed for teams preparing for Pathfinder Bible Experience. Learn more at <a href="https://nadpbe.org/">nadpbe.org</a>.</p>
		<div class="tech-pills" aria-label="PBE technologies">
			<button class="tech-pill tech-pill-link" type="button" data-filter="ASP.NET">ASP.NET</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="Blazor">Blazor</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="SQL Server">SQL Server</button>
			<button class="tech-pill tech-pill-link" type="button" data-filter="Azure App Service">Azure App Service</button>
		</div>
		<p><a href="/PBE/">View Project →</a></p>
	</article>
</div>

<style>
	.project-filters {
		display: flex;
		flex-wrap: wrap;
		gap: 0.45rem;
		margin: 1rem 0 0.4rem;
	}

	.filter-btn,
	.tech-pill {
		border: 1px solid #cad5df;
		border-radius: 999px;
		background: #f5f8fb;
		color: #213243;
		padding: 0.25rem 0.7rem;
		font-size: 0.82rem;
		line-height: 1.4;
	}

	.filter-btn,
	.tech-pill-link {
		cursor: pointer;
	}

	.filter-btn:hover,
	.tech-pill-link:hover {
		background: #e8f0f7;
	}

	.filter-btn.active {
		border-color: #2d6da3;
		background: #2d6da3;
		color: #ffffff;
	}

	.filter-status {
		margin: 0.35rem 0 1rem;
		color: #4a5d70;
		font-size: 0.95rem;
	}

	.project-grid {
		display: grid;
		gap: 0.9rem;
	}

	.project-card {
		border: 1px solid #dbe3ea;
		border-radius: 10px;
		padding: 0.9rem 1rem;
		background: #ffffff;
	}

	.project-card h3 {
		margin: 0 0 0.45rem;
	}

	.project-card p {
		margin: 0.4rem 0;
	}

	.tech-pills {
		margin: 0.55rem 0 0.2rem;
		display: flex;
		flex-wrap: wrap;
		gap: 0.4rem;
	}

	@media (max-width: 640px) {
		.project-card {
			padding: 0.8rem;
		}
	}
</style>

<script>
	(function () {
		var grid = document.getElementById("project-grid");
		if (!grid) return;

		var cards = Array.prototype.slice.call(grid.querySelectorAll(".project-card"));
		var filterButtons = Array.prototype.slice.call(document.querySelectorAll(".filter-btn"));
		var pillButtons = Array.prototype.slice.call(document.querySelectorAll(".tech-pill-link"));
		var status = document.getElementById("filter-status");

		function setActive(value) {
			filterButtons.forEach(function (btn) {
				btn.classList.toggle("active", btn.getAttribute("data-filter") === value);
			});
		}

		function applyFilter(value) {
			var visibleCount = 0;

			cards.forEach(function (card) {
				var rawTech = card.getAttribute("data-tech") || "";
				var tech = rawTech.split("|");
				var show = value === "all" || tech.indexOf(value) !== -1;
				card.style.display = show ? "block" : "none";
				if (show) visibleCount += 1;
			});

			setActive(value);

			if (!status) return;
			if (value === "all") {
				status.textContent = "Showing all projects.";
			} else {
				status.textContent = "Showing " + visibleCount + " project" + (visibleCount === 1 ? "" : "s") + " using " + value + ".";
			}
		}

		filterButtons.forEach(function (btn) {
			btn.addEventListener("click", function () {
				applyFilter(btn.getAttribute("data-filter") || "all");
			});
		});

		pillButtons.forEach(function (pill) {
			pill.addEventListener("click", function () {
				applyFilter(pill.getAttribute("data-filter") || "all");
			});
		});
	})();
</script>

---

*More projects coming soon.*
