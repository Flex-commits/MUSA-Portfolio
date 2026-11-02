---
layout: post
title: 'Finding Support'
permalink: /projects/finding-support/
thumbnail: /assets/maps/finding-support/finding-support-poster.png
---

# Finding Support

**NYC homelessness services and nearby rail**<br>
30-Day Map Challenge · Day 2: Lines · November 2026

Where can someone go for help in NYC, and how close is it to the train?

For this map, I brought together 21 publicly listed service access points: adult drop-in centers, shelter intake centers, and youth drop-in centers. I then connected each address to its nearest subway or Staten Island Railway station. The lines show straight-line distance, rather than walking routes.

Housing and public health are connected, and I wanted this project to focus on a practical question about where support is located. The map lets you filter by service type and borough, see who each location serves, and compare its distance from rail.

<p><a href="https://flex-commits.github.io/30-days-mapping/finding-support/" target="_blank" rel="noopener" style="display:inline-block;padding:12px 18px;background:#25282d;color:#fff;text-decoration:none;">Open the interactive map ↗</a></p>

<iframe src="https://flex-commits.github.io/30-days-mapping/finding-support/" title="Finding Support: NYC services and nearby rail" loading="lazy" style="width:100%;height:860px;border:1px solid #dfe5e2;border-radius:3px;"></iframe>

The map, scripts, saved data and outputs live in my [separate map repository](https://github.com/Flex-commits/30-days-mapping/tree/main/day02-finding-support). This portfolio page links to that project.

## What the lines show

Each connection runs from an approximate service address to the nearest MTA station centroid. I calculated the distances against all 496 station records in the saved MTA dataset, using the haversine formula.

The longest connection is the youth drop-in location in Port Richmond: approximately 2.99 miles from Tompkinsville on the Staten Island Railway. That is a rail-proximity measurement. Bus and ferry connections, actual street routes, station entrances and step-free access would be the next things to add.

Select a location to see the station name, approximate distance, hours, audience, and official service information.

## Data and limits

The service directory comes from [NYC311 adult drop-in listings](https://portal.311.nyc.gov/article/?kanumber=KA-02528), [NYC311 shelter intake guidance](https://portal.311.nyc.gov/article/?kanumber=KA-02501), and [NYC DYCD youth drop-in listings](https://www.nyc.gov/site/dycd/services/runaway-homeless-youth/borough-based-drop-in-centers.page). Rail locations come from [MTA Subway Stations](https://data.ny.gov/Transportation/MTA-Subway-Stations/39hk-dx4f), which includes Staten Island Railway.

This is a snapshot checked on November 2, 2026. It covers public service access points, rather than all shelters. The service coordinates are Census address interpolations; the lines are not verified walking paths. A shorter line does not establish that a service is easier to reach or that a bed is available. Check eligibility and hours through the official listing before travel.

[Download the map image]({{ '/assets/maps/finding-support/finding-support-poster.png' | relative_url }}) · [Download the line data](https://flex-commits.github.io/30-days-mapping/finding-support/data/rail-links.geojson) · [Code and saved inputs](https://github.com/Flex-commits/30-days-mapping/tree/main/day02-finding-support)

<details>
<summary>Tools, credits and design references</summary>
<p>Made with Python, Matplotlib and Leaflet. Borough geometry: NYC Department of City Planning. Regional land: Natural Earth. Optional street context: OpenStreetMap contributors. Typography: DM Sans. Research, code and editing were assisted by AI. Design references include <a href="https://work.co/clients/mta/">Work &amp; Co’s MTA map</a> and <a href="https://morphocode.com/announcing-urban-layers/">Morphocode’s Urban Layers</a>.</p>
</details>
