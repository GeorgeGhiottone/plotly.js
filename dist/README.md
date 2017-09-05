# Using distributed files

All plotly.js dist bundles inject an object `Plotly` into the global scope.

Import plotly.js as:

```html
<script type="text/javascript" src="plotly.min.js"></script>
```

or the un-minified version as:

```html
<script type="text/javascript" src="plotly.js" charset="utf-8"></script>
```

To support IE9, put:

```html
<script>if(typeof window.Int16Array !== 'function')document.write("<scri"+"pt src='extras/typedarray.min.js'></scr"+"ipt>");</script>
<script>document.write("<scri"+"pt src='extras/request_animation_frame.js'></scr"+"ipt>");</script>
```

before the plotly.js script tag.

To add MathJax, put

```html
<script type="text/javascript" src="mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>
```

before the plotly.js script tag. You can grab the relevant MathJax files in `./dist/extras/mathjax/`.

# Bundle information

The main plotly.js bundle includes all the official (non-beta) trace modules.

It be can imported as minified javascript
- using dist file `dist/plotly.min.js`
- using CDN URL https://cdn.plot.ly/plotly-latest.min.js OR https://cdn.plot.ly/plotly-1.30.0.min.js

or as raw javascript:
- using dist file `dist/plotly.js`
- using CDN URL https://cdn.plot.ly/plotly-latest.js OR https://cdn.plot.ly/plotly-1.30.0.js
- using CommonJS with `require('plotly.js')`

If you would like to have access to the attribute meta information (including attribute descriptions as on the [schema reference page](https://plot.ly/javascript/reference/)), use dist file `dist/plotly-with-meta.js`

The main plotly.js bundle weights in at:

| plotly.js | plotly.min.js | plotly.min.js + gzip | plotly-with-meta.js |
|-----------|---------------|----------------------|---------------------|
<<<<<<< HEAD
| 5.2 MB | 2.1 MB | 634.9 kB | 5.3 MB |
=======
<<<<<<< HEAD
| 5.1 MB | 2.1 MB | 631.2 kB | 5.3 MB |
=======
| 5.5 MB | 2.2 MB | 672.1 kB | 5.6 MB |
>>>>>>> upstream/master
>>>>>>> origin/master

## Partial bundles

Starting in `v1.15.0`, plotly.js also ships with several _partial_ bundles:

- [basic](#plotlyjs-basic)
- [cartesian](#plotlyjs-cartesian)
- [geo](#plotlyjs-geo)
- [gl3d](#plotlyjs-gl3d)
- [gl2d](#plotlyjs-gl2d)
- [mapbox](#plotlyjs-mapbox)
- [finance](#plotlyjs-finance)

### plotly.js basic

The `basic` partial bundle contains the `scatter`, `bar` and `pie` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-basic.js` |
| dist bundle (minified) | `dist/plotly-basic.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-basic-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-basic-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-basic-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-basic-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-basic')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 1.7 MB | 650.3 kB | 212 kB |
=======
<<<<<<< HEAD
| 1.7 MB | 646.4 kB | 210.3 kB |
=======
| 1.8 MB | 676 kB | 220.1 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js cartesian

The `cartesian` partial bundle contains the `scatter`, `bar`, `box`, `heatmap`, `histogram`, `histogram2d`, `histogram2dcontour`, `pie`, `contour` and `scatterternary` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-cartesian.js` |
| dist bundle (minified) | `dist/plotly-cartesian.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-cartesian-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-cartesian-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-cartesian-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-cartesian-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-cartesian')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 1.9 MB | 725.3 kB | 234.6 kB |
=======
<<<<<<< HEAD
| 1.9 MB | 721.4 kB | 232.8 kB |
=======
| 2 MB | 759.1 kB | 245.6 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js geo

The `geo` partial bundle contains the `scatter`, `scattergeo` and `choropleth` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-geo.js` |
| dist bundle (minified) | `dist/plotly-geo.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-geo-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-geo-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-geo-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-geo-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-geo')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 1.7 MB | 673.2 kB | 220.5 kB |
=======
<<<<<<< HEAD
| 1.7 MB | 669.3 kB | 218.9 kB |
=======
| 1.8 MB | 698.5 kB | 228.5 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js gl3d

The `gl3d` partial bundle contains the `scatter`, `scatter3d`, `surface` and `mesh3d` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-gl3d.js` |
| dist bundle (minified) | `dist/plotly-gl3d.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-gl3d-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-gl3d-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-gl3d-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-gl3d-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-gl3d')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 2.6 MB | 1.1 MB | 349.8 kB |
=======
<<<<<<< HEAD
| 2.6 MB | 1.1 MB | 344 kB |
=======
| 2.7 MB | 1.1 MB | 358.4 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js gl2d

The `gl2d` partial bundle contains the `scatter`, `scattergl`, `pointcloud`, `heatmapgl`, `contourgl` and `parcoords` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-gl2d.js` |
| dist bundle (minified) | `dist/plotly-gl2d.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-gl2d-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-gl2d-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-gl2d-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-gl2d-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-gl2d')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 2.7 MB | 1.1 MB | 356.6 kB |
=======
<<<<<<< HEAD
| 2.7 MB | 1.1 MB | 353.5 kB |
=======
| 2.8 MB | 1.1 MB | 367.8 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js mapbox

The `mapbox` partial bundle contains the `scatter` and `scattermapbox` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-mapbox.js` |
| dist bundle (minified) | `dist/plotly-mapbox.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-mapbox-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-mapbox-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-mapbox-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-mapbox-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-mapbox')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 2.8 MB | 1.1 MB | 324.9 kB |
=======
<<<<<<< HEAD
| 2.8 MB | 1.1 MB | 322.8 kB |
=======
| 2.9 MB | 1.1 MB | 333.6 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

### plotly.js finance

The `finance` partial bundle contains the `scatter`, `bar`, `histogram`, `pie`, `ohlc` and `candlestick` trace modules.

| Way to import | Location |
|---------------|----------|
| dist bundle | `dist/plotly-finance.js` |
| dist bundle (minified) | `dist/plotly-finance.min.js` |
| CDN URL (latest) | https://cdn.plot.ly/plotly-finance-latest.js |
| CDN URL (latest minified) | https://cdn.plot.ly/plotly-finance-latest.min.js |
| CDN URL (tagged) | https://cdn.plot.ly/plotly-finance-1.30.0.js |
| CDN URL (tagged minified) | https://cdn.plot.ly/plotly-finance-1.30.0.min.js |
| CommonJS | `require('plotly.js/lib/index-finance')` |

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 1.8 MB | 677.1 kB | 219.6 kB |
=======
<<<<<<< HEAD
| 1.8 MB | 673.2 kB | 217.9 kB |
=======
| 1.9 MB | 704.3 kB | 228.2 kB |
>>>>>>> upstream/master
>>>>>>> origin/master

----------------

_This file is auto-generated by `npm run stats`. Please do not edit this file directly._
