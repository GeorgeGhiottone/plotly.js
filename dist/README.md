# Using distributed files

All plotly.js dist bundles inject an object `Plotly` into the global scope.

Import plotly.js as:

```html
<script src="plotly.min.js"></script>
```

or the un-minified version as:

```html
<script src="plotly.js" charset="utf-8"></script>
```

### To support IE9

*Before* the plotly.js script tag, add:

```html
<script>if(typeof window.Int16Array !== 'function')document.write("<scri"+"pt src='extras/typedarray.min.js'></scr"+"ipt>");</script>
<script>document.write("<scri"+"pt src='extras/request_animation_frame.js'></scr"+"ipt>");</script>
```

### To support MathJax

*Before* the plotly.js script tag, add:

```html
<script src="mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>
```

You can grab the relevant MathJax files in `./dist/extras/mathjax/`.

### To include localization

Plotly.js defaults to US English (en-US) and includes British English (en) in the standard bundle.
Many other localizations are available - here is an example using Swiss-German (de-CH),
see the contents of this directory for the full list.
They are also available on our CDN as https://cdn.plot.ly/plotly-locale-de-ch-latest.js OR https://cdn.plot.ly/plotly-locale-de-ch-1.39.4.js
Note that the file names are all lowercase, even though the region is uppercase when you apply a locale.

*After* the plotly.js script tag, add:

```html
<script src="plotly-locale-de-ch.js"></script>
<script>Plotly.setPlotConfig({locale: 'de-CH'})</script>
```

The first line loads and registers the locale definition with plotly.js, the second sets it as the default for all Plotly plots.
You can also include multiple locale definitions and apply them to each plot separately as a `config` parameter:

```js
Plotly.newPlot(graphDiv, data, layout, {locale: 'de-CH'})
```

# Bundle information

The main plotly.js bundle includes all the official (non-beta) trace modules.

It be can imported as minified javascript
- using dist file `dist/plotly.min.js`
- using CDN URL https://cdn.plot.ly/plotly-latest.min.js OR https://cdn.plot.ly/plotly-1.39.4.min.js

or as raw javascript:
- using the `plotly.js-dist` npm package (starting in `v1.39.0`)
- using dist file `dist/plotly.js`
- using CDN URL https://cdn.plot.ly/plotly-latest.js OR https://cdn.plot.ly/plotly-1.39.4.js
- using CommonJS with `require('plotly.js')`

If you would like to have access to the attribute meta information (including attribute descriptions as on the [schema reference page](https://plot.ly/javascript/reference/)), use dist file `dist/plotly-with-meta.js`

The main plotly.js bundle weights in at:

| plotly.js | plotly.min.js | plotly.min.js + gzip | plotly-with-meta.js |
|-----------|---------------|----------------------|---------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 5.1 MB | 2.1 MB | 631.2 kB | 5.3 MB |
=======
| 5.5 MB | 2.2 MB | 672.1 kB | 5.6 MB |
>>>>>>> upstream/master
=======
| 5.7 MB | 2.7 MB | 811.3 kB | 5.9 MB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

## Partial bundles

Starting in `v1.15.0`, plotly.js also ships with several _partial_ bundles:

- [basic](#plotlyjs-basic)
- [cartesian](#plotlyjs-cartesian)
- [geo](#plotlyjs-geo)
- [gl3d](#plotlyjs-gl3d)
- [gl2d](#plotlyjs-gl2d)
- [mapbox](#plotlyjs-mapbox)
- [finance](#plotlyjs-finance)

Starting in `v1.39.0`, each plotly.js partial bundle has a corresponding npm package with no dependencies.
### plotly.js basic

The `basic` partial bundle contains trace modules `scatter`, `bar` and `pie`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
| 2.1 MB | 760.1 kB | 247.9 kB |

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-basic-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-basic-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-basic-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-basic-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-basic-dist`](https://www.npmjs.com/package/plotly.js-basic-dist) with
```
npm install plotly.js-basic-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-basic-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-basic-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-basic.js` |
| dist bundle (minified) | `dist/plotly-basic.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-basic'` |
| CommonJS | `require('plotly.js/lib/index-basic')` |


### plotly.js cartesian

The `cartesian` partial bundle contains trace modules `scatter`, `bar`, `box`, `heatmap`, `histogram`, `histogram2d`, `histogram2dcontour`, `pie`, `contour`, `scatterternary` and `violin`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 1.7 MB | 646.4 kB | 210.3 kB |
=======
| 1.8 MB | 676 kB | 220.1 kB |
>>>>>>> upstream/master
=======
| 2.4 MB | 870.7 kB | 282.3 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-cartesian-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-cartesian-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-cartesian-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-cartesian-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-cartesian-dist`](https://www.npmjs.com/package/plotly.js-cartesian-dist) with
```
npm install plotly.js-cartesian-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-cartesian-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-cartesian-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-cartesian.js` |
| dist bundle (minified) | `dist/plotly-cartesian.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-cartesian'` |
| CommonJS | `require('plotly.js/lib/index-cartesian')` |


### plotly.js geo

The `geo` partial bundle contains trace modules `scatter`, `scattergeo` and `choropleth`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 1.9 MB | 721.4 kB | 232.8 kB |
=======
| 2 MB | 759.1 kB | 245.6 kB |
>>>>>>> upstream/master
=======
| 2.1 MB | 783.6 kB | 257 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-geo-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-geo-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-geo-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-geo-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-geo-dist`](https://www.npmjs.com/package/plotly.js-geo-dist) with
```
npm install plotly.js-geo-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-geo-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-geo-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-geo.js` |
| dist bundle (minified) | `dist/plotly-geo.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-geo'` |
| CommonJS | `require('plotly.js/lib/index-geo')` |


### plotly.js gl3d

The `gl3d` partial bundle contains trace modules `scatter`, `scatter3d`, `surface`, `mesh3d`, `cone` and `streamtube`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 1.7 MB | 669.3 kB | 218.9 kB |
=======
| 1.8 MB | 698.5 kB | 228.5 kB |
>>>>>>> upstream/master
=======
| 3.2 MB | 1.3 MB | 404.7 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-gl3d-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-gl3d-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-gl3d-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-gl3d-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-gl3d-dist`](https://www.npmjs.com/package/plotly.js-gl3d-dist) with
```
npm install plotly.js-gl3d-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-gl3d-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-gl3d-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-gl3d.js` |
| dist bundle (minified) | `dist/plotly-gl3d.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-gl3d'` |
| CommonJS | `require('plotly.js/lib/index-gl3d')` |


### plotly.js gl2d

The `gl2d` partial bundle contains trace modules `scatter`, `scattergl`, `splom`, `pointcloud`, `heatmapgl`, `contourgl` and `parcoords`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 2.6 MB | 1.1 MB | 344 kB |
=======
| 2.7 MB | 1.1 MB | 358.4 kB |
>>>>>>> upstream/master
=======
| 3.2 MB | 1.3 MB | 426.3 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-gl2d-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-gl2d-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-gl2d-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-gl2d-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-gl2d-dist`](https://www.npmjs.com/package/plotly.js-gl2d-dist) with
```
npm install plotly.js-gl2d-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-gl2d-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-gl2d-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-gl2d.js` |
| dist bundle (minified) | `dist/plotly-gl2d.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-gl2d'` |
| CommonJS | `require('plotly.js/lib/index-gl2d')` |


### plotly.js mapbox

The `mapbox` partial bundle contains trace modules `scatter` and `scattermapbox`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 2.7 MB | 1.1 MB | 353.5 kB |
=======
| 2.8 MB | 1.1 MB | 367.8 kB |
>>>>>>> upstream/master
=======
| 2.6 MB | 1.3 MB | 394.8 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-mapbox-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-mapbox-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-mapbox-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-mapbox-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-mapbox-dist`](https://www.npmjs.com/package/plotly.js-mapbox-dist) with
```
npm install plotly.js-mapbox-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-mapbox-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-mapbox-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-mapbox.js` |
| dist bundle (minified) | `dist/plotly-mapbox.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-mapbox'` |
| CommonJS | `require('plotly.js/lib/index-mapbox')` |


### plotly.js finance

The `finance` partial bundle contains trace modules `scatter`, `bar`, `histogram`, `pie`, `ohlc` and `candlestick`.

#### Stats

| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
<<<<<<< HEAD
| 2.8 MB | 1.1 MB | 322.8 kB |
=======
| 2.9 MB | 1.1 MB | 333.6 kB |
>>>>>>> upstream/master
=======
| 2.2 MB | 790.4 kB | 257 kB |
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

#### CDN links

| Flavor | URL |
| ------ | --- |
| Latest | https://cdn.plot.ly/plotly-finance-latest.js |
| Latest minified | https://cdn.plot.ly/plotly-finance-latest.min.js |
| Tagged | https://cdn.plot.ly/plotly-finance-1.39.4.js |
| Tagged minified | https://cdn.plot.ly/plotly-finance-1.39.4.min.js |

#### npm package (starting in `v1.39.0`)

Install [`plotly.js-finance-dist`](https://www.npmjs.com/package/plotly.js-finance-dist) with
```
npm install plotly.js-finance-dist
```

ES6 module usage:
```js
import Plotly from 'plotly.js-finance-dist'
```

CommonJS usage:
```js
var Plotly = require('plotly.js-finance-dist');
```

#### Other plotly.js entry points

| Flavor | Location |
|---------------|----------|
| dist bundle | `dist/plotly-finance.js` |
| dist bundle (minified) | `dist/plotly-finance.min.js` |
| ES6 module | `import Plotly from 'plotly.js/lib/index-finance'` |
| CommonJS | `require('plotly.js/lib/index-finance')` |

<<<<<<< HEAD
| Raw size | Minified size | Minified + gzip size |
|------|-----------------|------------------------|
<<<<<<< HEAD
| 1.8 MB | 673.2 kB | 217.9 kB |
=======
| 1.9 MB | 704.3 kB | 228.2 kB |
>>>>>>> upstream/master
=======
>>>>>>> def6aa5a24527c68e90f50485255170609640e43

----------------

_This file is auto-generated by `npm run stats`. Please do not edit this file directly._