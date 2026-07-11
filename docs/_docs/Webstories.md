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

## Creating a story

1. Go to **Web Stories** in the using the Naviagation menu on the left side of the screen.
> **Note 1:** The navigation menu can be expanded or collapsed using the arrow button(|-> OR <-| respectively).
![Web Stories page with collapsed menu](../_static/images/webstories/02_landing_page_collapsed_menu.png "Web Stories page with collapsed menu")

2. Click **Create New Story**.
> **Note 2:** On smaller screens, the navigation menu may shrink into a menu button (three horizontal lines inside a black square) located in the top-left corner of the screen. Tap or click this button to open the menu.

> **Note 3:** Like **Note 2**, the **Create New Story** button may be shrunk into a menu button (three horizontal lines with a white background, next to the "Dashboard" title). Tap or click this button to open the menu.

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <img src="../_static/images/webstories/03_landing_page_small_screen_collapsed_menu.png" alt="Small screen with the navigation menu collapsed" title="Collapsed Menu View" style="width: 32%;" />
  <img src="../_static/images/webstories/04_landing_page_small_screen_expanded_menu.png" alt="Small screen with the navigation menu expanded" title="Expanded Menu View" style="width: 32%;" />
  <img src="../_static/images/webstories/05_landing_page_small_screen_expanded_menu_webstories.png" alt="Small screen showing the expanded Web Stories specific menu" title="Web Stories Menu View" style="width: 32%;" />
</div>

3. Fill in the story title, then save as a draft:
![Web Stories editing canvas](../_static/images/webstories/06_webstories_editing_canvas.png "Web Stories editing canvas")

> **Note 4:** A story can be published with a blank title, ClimWeb will default the title to "Untitled." in this scenario.

4. Save the story by selecting *Save draft* in the bottom left of the screen. The other fields will be covered later in this guide (see Media and text overlays and Publishing).

> **Tip:** You can create the story with just a title first, then build out content. You do not need to have every field filled in before adding content.

## Troubleshooting

| Problem | Likely cause | What to do |
|---|---|---|
| Images fail to load in the story editor, browser console shows a CORS error | `WAGTAILADMIN_BASE_URL` and/or the Wagtail Site record does not match the host/port actually being used | Align both to the same value (e.g. `http://localhost:8000`) and restart the server |