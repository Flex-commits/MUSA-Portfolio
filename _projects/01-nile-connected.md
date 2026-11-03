---
layout: post
title: 'The Nile, Connected'
permalink: /projects/nile-connected/
thumbnail: /assets/maps/nile/02-thomas-hagos.png
---

# The Nile, Connected

**One basin, many tributaries.**<br>
30-Day Map Challenge · Day 2: Lines · November 2026

I followed the Nile upstream: through Sudan, into the Ethiopian highlands and the equatorial lake catchments. I wanted the branching network to be the subject of this map.

The map contains 133,797 connected river reaches from HydroRIVERS. Pale gold traces the White Nile system, amber the Blue Nile system, and coral the Atbara system. The remaining connected Nile network is blue-gray. The navy background, cream type and warm accents continue the style of my Day 1 map, The Restless Earth. Line thickness follows Strahler stream order.

[Open the project and full-resolution map](https://flex-commits.github.io/30-days-mapping/nile/) · [Code and sources](https://github.com/Flex-commits/30-days-mapping/tree/main/day02-nile)

![The Nile connected river network](https://flex-commits.github.io/30-days-mapping/nile/nile-connected.png)

## How I made it

I used HydroBASINS’ Nile drainage boundary, then followed HydroRIVERS’ downstream identifiers to retain the connected network. Reverse traversal from the White Nile, Blue Nile and Atbara confluences assigns the tributary colors. Every retained downstream endpoint matches its next reach, and every path terminates at the modeled outlet.

The full methods, source manifest, dependency versions and reproduction scripts live in my separate [30-days-mapping repository](https://github.com/Flex-commits/30-days-mapping/tree/main/day02-nile).

## What to keep in mind

These are modeled drainage lines, including channels that may be dry or intermittent. The source omits smaller streams below its inclusion thresholds. The broad basin outline includes some enclosed drainage areas excluded from the connected river network. The source routes the Nile to one Mediterranean outlet and does not show every delta branch or canal. Lake crossings are modeled routing, not surveyed channels across open water. This is not a current-flow or navigation map.

HydroRIVERS and HydroBASINS: WWF / McGill University, accessed through UNESCO IHP-WINS. Context: Natural Earth. River names and geographic relationships checked against Nile Basin Initiative references. Map by Thomas Hagos, made with Python, GeoPandas and Matplotlib. Research, code and editing were assisted by AI. Full attribution and license links are on the project page and in the source repository.
