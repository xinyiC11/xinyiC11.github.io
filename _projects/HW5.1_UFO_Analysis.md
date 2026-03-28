---
layout: project
title: "Global UFO Sightings Analysis"
caption: "Interactive Data Visualization using Python and Vega-Lite"
description: "A comprehensive look at UFO shape distributions and sighting durations across the globe."
image: https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv 
---

# IS445 Homework 5.1 UFO Data Visualization

In this project, I used Python, Altair, and Vega-Lite to analyze a dataset of global UFO sightings. The goal was to transform raw data into insights through effective encoding and interactivity.

---

## Visualization 1: Frequency of Reported UFO Shapes

This horizontal bar chart visualizes the distribution of different UFO shapes reported in the dataset. I used a horizontal bar chart where the y-axis represents the **nominal** encoding for the UFO shapes, and the x-axis represents the **quantitative** count of sightings. The shapes are sorted to quickly identify the most common types. For design, I chose **'steelblue'** to maintain visual clarity.

<div id="vis1"></div>

---

## Visualization 2: Sighting Duration Over Time (Interactive)

The second plot explores the relationship between the date of a sighting and the total duration in seconds. I used **temporal** encoding for the x-axis and **quantitative** encoding for the y-axis. Due to the extreme variance in duration values, I applied a **logarithmic scale** to the y-axis to reveal hidden patterns. The points are colored based on the **nominal** 'shape' variable, using the default Altair color scheme to help distinguish between different UFO types.

**Interactivity Discussion:**
For this visualization, I implemented a **tooltip** and a **year slider**. The tooltip allows users to hover over any data point to view specific details like the city, shape, and duration. The year slider provides a crucial interactive filter that manages the high density of points; it helps users focus on sightings from a specific year, making the entire visualization much clearer and more suitable for granular analysis. This combination of Log Scale and Interactivity enables a better understanding of patterns over time within a complex dataset.
<div id="vis2"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
  var spec1 = "{{ site.baseurl }}/ufo_shapes.json";
  var spec2 = "{{ site.baseurl }}/ufo_interactive.json";

  vegaEmbed('#vis1', spec1).catch(console.error);
  vegaEmbed('#vis2', spec2).catch(console.error);
</script>

### Links
- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
- [The Analysis (GitHub Notebook)](https://github.com/xinyiC11/xinyiC11.github.io/blob/main/IS445_HW5_1.ipynb)
