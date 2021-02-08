# How to reduce GeoJSON file size with mapshaper.org

GeoJSON and shapfiles can be a few hundred megabytes, and that becomes a problem when you are trying to make interactive online maps where the webpage size should be small.

https://mapshaper.org/ to the rescue! No installation whatever, all inside a browser, yet super fast.

But there are [some problems](https://community.plotly.com/t/choropleth-map-not-working-with-my-geojson-data/43934/2) still if you use the converted files with plotly for making choropleths. Hence this guide:

## Step 1: Import file

Go to https://mapshaper.org/ and import your GeoJSON file.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/1.PNG" width=800>

## Step 2
Make sure "detect line intersection" is checked.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/2.PNG" width=800>

## Step 3
If you map loads correctly, click "Simplify".


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/3.PNG" width=800>

## Step 4
Tick "prevent shape removal", use "Visvalingam / weigthed area" if you don't have other preferences and apply.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/4.PNG" width=800>

## Step 5
Move the slider to any percentage. If your initial filesize is 100 MB and you slide to 1%, then output file will be 1% of 100 MB. Also click "Repair" after sliding.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/5.PNG" width=800>

## Step 6
Now click export.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/6.PNG" width=800>

## Step 7
Use whatever output format you please, but for compatibility with plotly and D3.js, you should include the output parameter `gj2008` to export properly.


<img src="https://github.com/yasserius/mapshaper_geojson_simplify/blob/main/7.PNG" width=800>

And you're done! yay

