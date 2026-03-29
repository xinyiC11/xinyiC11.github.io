---
name: UFO Sightings Analysis
tools: [Python]
image: assets/pngs/visualization.png
description: An interactive visualization of UFO shapes and their distribution over time.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# UFO Sightings Exploration

This project analyzes the UFO sightings dataset to uncover patterns in reported alien encounters. The goal is to visualize how sighting shapes vary and how these reports have changed over time.

## Visualization 1: UFO Shapes Distribution

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufo_shapes.json" style="width: 100%"></vegachart>

**Write-up for Plot 1:**
This bar chart shows the total count of sightings for each UFO shape. I used Nominal encoding for the x-axis (shapes) and Quantitative encoding for the y-axis (count). I applied a categorical color scheme based on the "shape" variable to make different categories easier to distinguish. For data transformation, I used Pandas in my Python notebook to group the data by shape and filter out null values, ensuring only valid shape records are displayed.

## Visualization 2: Temporal Trends & Interactive Exploration

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufo_interactive.json" style="width: 100%"></vegachart>

**Write-up for Plot 2 & Interactivity:**
This line chart visualizes the number of sightings over the years using Temporal encoding for the x-axis. To make the chart interactive, I added a dropdown selection filter for UFO shapes. This allows users to pick a specific shape and see its individual trend, which helps reduce visual clutter compared to showing all lines at once. In Python, I transformed the date column into a proper datetime format and aggregated the sightings by year to create a smooth timeline.

---

## Data & Methods

As per the requirements, here are the links to the original data source and the analysis notebook:

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/xinyiC11/xinyiC11.github.io/blob/main/python_notebooks/IS445_HW5_1.ipynb" text="The Analysis" %}
</div>

