---
layout: page
title: BiblePaths.NET
permalink: /BiblePaths/
tech:
	- ASP.NET
	- Razor Pages
	- Blazor
	- SQL Server
	- Azure App Service
	- OpenAI API
---

## BiblePaths.NET

<div class="tech-pills" aria-label="Technologies used">
	{% for t in page.tech %}
	<span class="tech-pill">{{ t }}</span>
	{% endfor %}
</div>

**Live Site:** [BiblePaths.NET](https://biblepaths.net)

Bible Paths is a full stack crowd sourced Bible study and devotional tool. Each Bible Path is a chain of Bible verses linked together to form a simple, self contained Bible study. 

<style>
	.tech-pills {
		margin: 0.75rem 0 1rem;
	}

	.tech-pill {
		display: inline-block;
		margin: 0 0.45rem 0.45rem 0;
		padding: 0.2rem 0.65rem;
		border: 1px solid #cad5df;
		border-radius: 999px;
		background: #f5f8fb;
		color: #213243;
		font-size: 0.82rem;
		line-height: 1.45;
	}
</style>

---

### Features

- 🔗 **User Contributed Paths** — Logged in Users are able to build/publish their own paths
- 🔍 **Path finder** — Discover meaningful paths by rating, topics, and AI 
- 📖 **AI Path Summarization** — Paths are summarized using AI for comprehensive search
---

### Screenshots

![BiblePaths Home](HomePage001.png)
![Path Builder](FollowPath.png)
![Follow a Path](FollowPath.png)


---

### About the Project

BiblePaths.NET was built to make scripture exploration more intuitive and discovery-driven. Rather than searching for a specific verse, users can wander through connections and uncover passages they might never have found otherwise.

**Tech stack:** 
- Azure hosted ASP.Net Web App with a mix of Razor and Blazor Pages
- API layer for automation
- Google and Microsoft based Authentication
- SQL Database

---

[← Back to all projects](/)
