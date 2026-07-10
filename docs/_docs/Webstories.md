# Creating and publishing Web Stories

## Introduction

Web Stories are short, full-screen videos(similar to those found on various social media platforms) built on Google's open Web Stories standard. They are designed for quick, mobile-first storytelling using images, videos and short texts that readers tap through one at a time.

For National Meteorological and Hydrological Service(NMHS), Web Stories are a good fit for content that benefits from a qucik visual format rather than a a long article. For example, a seasonal outlook explainer or public awareness campaign.

In ClimWeb, Web Stories are managed from the **Web Stories** section. Published stories are automatically included in the site's sitemap, hencing making them easier to search for.

This guide walks through the full workflow: Creating a story, adding and ordering slides, adding media and text overlays, previewing, publishing and managing stories after they are published.

![Web Stories landing page](../_static/images/webstories/01_landing_page.png "Web Stories landing page")

## Prerequisites

Before creating your first Web Story, verify the following, especially on a freshly installed instance:

1. **A Home Page must exist and be published.** 
A fresh ClimWeb checkout has no pages beyond Wagtail's generic "Welcome to your new Wagtail site" placeholder. Create and publish a real Home Page first (select *Pages*, select *Add child page*, fill in required fields, Publish), and confirm it is set as the site's root page under *Settings*, *Sites*.

2. **A Web Stories listing page must exist and be published as a child of Home page.**
Without one, the Web Stories dashboard (`/cms-admin/web-stories-list/`) returns a server error, and the editor may not function correctly. To create it: select *Pages*, open *Home*, select *Add child page*, select *Web Story List Page*, give it a title (e.g. "Web Stories"), select *Publish*. Only one instance of this page is needed per site.


## Troubleshooting

| Problem | Likely cause | What to do |
|---|---|---|
| Images fail to load in the story editor, browser console shows a CORS error | `WAGTAILADMIN_BASE_URL` and/or the Wagtail Site record does not match the host/port actually being used | Align both to the same value (e.g. `http://localhost:8000`) and restart the server |