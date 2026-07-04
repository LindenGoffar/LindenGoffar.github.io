---
layout: page
title: PBE Quiz App
permalink: /PBE/
tech:
	- Blazor
	- ASP.NET
	- Azure App Service
	- SQL Server
---

## PBE Quiz App

<div class="tech-pills" aria-label="Technologies used">
	{% for t in page.tech %}
	<span class="tech-pill">{{ t }}</span>
	{% endfor %}
</div>

**Live Site:** [BiblePaths.NET/PBE](https://biblepaths.net/PBE)

powered by BiblePaths.Net
The Pathfinder Bible Experience (PBE) quiz app is designed for use by teams preparing for Pathfinder Bible Experience, for more information on this youth program see: https://nadpbe.org/

---

### Features

- 🔗 **Question Builder** — Users contribute questions grounded directly in the Bible Text
- ❓ **Quiz Experience** — Quizzes are run in app with time keeping and score tracking
- 📖 **Passage viewer** — Read referenced passages in context of a Question
- 🏷️ **Quiz History Tracking** — Teams can track their improvement over time

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

### Screenshots

Once you add images to this folder, display them like this:
![PBE home screen](PBEHome.png)
![Question view](PBEQuestion.png)

---

[← Back to all projects](/)
