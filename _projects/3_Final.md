---
name: Final Part 3
tools: [Python, HTML, vega-lite]
image: assets/pngs/visualization.png
description: GitHub page for HW 5.1
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


<h1 style="text-align: center;">Inflation-Adjusted Commodities with Ruling-Party Statistics (Republican vs. Democrat)</h1>
<div class="chart-breakout">
    <div class="chart-inner">
        <vegachart 
            schema-url="{{ site.baseurl }}/assets/json/visualization1.json" 
            style="width: 100%;">
        </vegachart>
    </div>
</div>

<style>
.chart-breakout {
    position: relative;
    /* This escapes the text container */
    width: 100vw;
    margin-left: calc(-50vw + 50%);
    
    /* This centers the content inside the new full-width area */
    display: flex;
    justify-content: center;
    align-items: center;
}

.chart-inner {
    width: 100%;
    /* Limits the map size so it's not literally touching the screen edges */
    max-width: 1200px; 
    padding: 0 20px;
}
</style>

### Description:
This plot shows the relationship between various extremely necessary commodities (Gas, Spaghetti, Ice Cream, Bacon, etc.) and the ruling party. Inflation year-over-year is measured by calculating the price increase in a "basket" of goods representative of what American's consider neccessary. Here, we show what each commodity would have cost in 2026 dollars from 1976 onwards. Sadly, there is very little data on spaghetti. 

We are primarily interested in whether the ruling party (Democrat/Republican) is potentially responsible for price increases, such as the recent war in Iran having significant impacts of the price of Gasoline. The background is highlighted in red/blue, indicating which political party holds most of the 3 branches of government. On the right, we see the specific makeup of the government for a selected range of years (averaged). This is useful for telling us whether there is a lame-duck president, wherein the legislative branch is split and little can be done, or there is a strong hold on power, such as in our current administration.

## Colormap:
I chose the ``dark2`` colormap because it's a bit more high-contrast than ``tableau10``, but I also added a drop-shadow to help it stand out against the red/blue shading. Obviously, the red/blue is indicative of Republican and Democrat, so there wasn't much flexibility there.

# Contextual Visualizations

<vegachart schema-url="{{ site.baseurl }}/assets/json/visualization2.json" style="width: 100%"></vegachart>

### Description:
This plot shows a map of the United States wherein each state is shaded according to the political affiliation of the sitting judges during a given selected year. On the right, we see the average of the basket of commodities for that selected year as well. This is an important contextual visualization, as it shows us something more long-term than representatives. Judges are often life-long appointments, or at the very least, served for many decades. A large shift in the political leaning of the overall Justice system can tell us a bit more about how laws are interpreted. In particular, these are Federally appointed judges, so cases tend to be significant in matter, rather than simple civil suits.

## Colormap:
The colormap is diverging between red and blue to best show the political lean, this is a common choice for politcal maps of the USA.

<h2 style="text-align: center;">Data & Notebook</h2>

<div class="left">
{% include elements/button.html link="https://github.com/nolan-cummins/nolan-cummins.github.io/tree/main/python_notebooks/data" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/nolan-cummins/nolan-cummins.github.io/blob/main/python_notebooks/final_3.1.ipynb" text="The Analysis" %}
</div>
