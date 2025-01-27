<a href="https://plotly.com/javascript/"><img src="https://images.plot.ly/logo/plotlyjs-logo@2x.png" height="70"></a>

[![npm version](https://badge.fury.io/js/plotly.js.svg)](https://badge.fury.io/js/plotly.js)
[![circle ci](https://circleci.com/gh/plotly/plotly.js.png?&style=shield&circle-token=1f42a03b242bd969756fc3e53ede204af9b507c0)](https://circleci.com/gh/plotly/plotly.js)
[![MIT License](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://github.com/plotly/plotly.js/blob/master/LICENSE)

[Plotly.js](https://plotly.com/javascript) is a standalone Javascript data visualization library, and it also powers the Python and R modules named `plotly` in those respective ecosystems (referred to as [Plotly.py](https://plotly.com/python) and [Plotly.R](http://plotly.com/r)).

Plotly.js can be used to produce dozens of chart types and visualizations, including statistical charts, 3D graphs, scientific charts, SVG and tile maps, financial charts and more.

<p align="center">
    <a href="https://plotly.com/javascript/" target="_blank">
        <img src="https://raw.githubusercontent.com/cldougl/plot_images/add_r_img/plotly_2017.png">
    </a>
</p>

[Contact us](https://plotly.com/products/consulting-and-oem/) for Plotly.js consulting, dashboard development, application integration, and feature additions.

## Table of contents

* [Load from npm (Node.js Package Manager)](#load-from-npm-nodejs-package-manager)
* [Load from Content Delivery Network (CDN)](#load-from-content-delivery-network-cdn)
* [Bundles](#bundles)
* [Alternative ways to require or build plotly.js](#alternative-ways-to-require-or-build-plotlyjs)
* [Documentation](#documentation)
* [Bugs and feature requests](#bugs-and-feature-requests)
* [Contributing](#contributing)
* [Notable contributors](#notable-contributors)
* [Copyright and license](#copyright-and-license)
* [Community](#community)

---
## Load from npm (Node.js Package Manager)

```sh
npm install plotly.js-dist-min
```

and import plotly.js as

```js
import Plotly from 'plotly.js-dist-min'
```
Or
```js
var Plotly = require('plotly.js-dist-min')
```

---
## Load from Content Delivery Network (CDN)
Fastly supports Plotly.js with free CDN service. Read more at <https://www.fastly.com/open-source>.

### Usage example
```html
<head>
    <script src="https://cdn.plot.ly/plotly-2.0.0-rc.3.min.js"></script>
</head>
<body>
    <div id="gd"></div>

    <script>
        Plotly.newPlot("gd", {
            "data": [{
                "y": [1, 2, 3]
            }],
            "layout": {
                "width": 600,
                "height": 400
            }
        });
    </script>
</body>
```
In the example above `Plotly` object is added to the window scope by the script in the `head` section.
The `newPlot` method is then used to draw an interactive figure as described by `data` and `layout` into the desired `div` here named `gd`.
As demonstrated in the example above basic knowledge of `html` and [JSON](https://en.wikipedia.org/wiki/JSON) syntax is enough to get started i.e. with/without JavaScript!
To learn and build more with plotly.js please visit [plotly.js documentation](https://plotly.com/javascript).

### Un-minified versions are also available on CDN
While non-minified source files may contain characters outside UTF-8, it is recommended that you specify the `charset` when loading those bundles.
```html
<script src="https://cdn.plot.ly/plotly-2.0.0-rc.3.js" charset="utf-8"></script>
```

> Please note that as of v2 the "plotly-latest" outputs (e.g. https://cdn.plot.ly/plotly-latest.min.js) will no longer be updated on the CDN, and will stay at the last v1 patch v1.58.4. Therefore, to use the CDN with plotly.js v2 and higher, you must specify an exact plotly.js version.

### To support MathJax
Load relevant MathJax (v2) files *Before* the plotly.js script tag:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS-MML_SVG.js"></script>
<script src="https://cdn.plot.ly/plotly-2.0.0-rc.3.min.js"></script>
```

## Bundles
There are two kinds of plotly.js bundles:
1. Complete and partial official bundles that are distributed to `npm` and the `CDN`, described in [the dist README](https://github.com/plotly/plotly.js/blob/master/dist/README.md).
2. Custom bundles you can create yourself to optimize the size of bundle depending on your needs. Please visit [CUSTOM_BUNDLE](https://github.com/plotly/plotly.js/blob/master/CUSTOM_BUNDLE.md) for more information.

---
## Alternative ways to require or build plotly.js
If your library needs to bundle or directly require [plotly.js/lib/index.js](https://github.com/plotly/plotly.js/blob/master/lib/index.js) or parts of its modules similar to [index-basic](https://github.com/plotly/plotly.js/blob/master/lib/index-basic.js) in some other way than via an official or a custom bundle, or in case you want to tweak the default build configurations of `browserify` or `webpack`, etc. then please visit [`BUILDING.md`](https://github.com/plotly/plotly.js/blob/master/BUILDING.md).

---
## Documentation

Official plotly.js documentation is hosted at [https://plotly.com/javascript](https://plotly.com/javascript).

These pages are generated by the Plotly [graphing-library-docs repo](https://github.com/plotly/graphing-library-docs) built with [Jekyll](https://jekyllrb.com/) and publicly hosted on GitHub Pages.
For more info about contributing to Plotly documentation, please read through [contributing guidelines](https://github.com/plotly/graphing-library-docs/blob/master/README.md).

---
## Bugs and feature requests

Have a bug or a feature request? Please [open a Github issue](https://github.com/plotly/plotly.js/issues/new) keeping in mind the [issue guidelines](https://github.com/plotly/plotly.js/blob/master/.github/ISSUE_TEMPLATE.md). You may also want to read about [how changes get made to Plotly.js](https://github.com/plotly/plotly.js/blob/master/CONTRIBUTING.md)


---
## Contributing

Please read through our [contributing guidelines](https://github.com/plotly/plotly.js/blob/master/CONTRIBUTING.md). Included are directions for opening issues, using plotly.js in your project and notes on development.

---
## Notable contributors

Plotly.js is at the core of a large and dynamic ecosystem with many contributors who file issues, reproduce bugs, suggest improvements, write code in this repo (and other upstream or downstream ones) and help users in the Plotly community forum. The following people deserve special recognition for their outsized contributions to this ecosystem:

|   | GitHub | Twitter | Status |
|---|--------|---------|--------|
|**Alex C. Johnson**| [@alexcjohnson](https://github.com/alexcjohnson) | | Active, Maintainer |
|**Mojtaba Samimi** | [@archmoj](https://github.com/archmoj) | [@solarchvision](https://twitter.com/solarchvision) | Active, Maintainer |
|**Antoine Roy-Gobeil** | [@antoinerg](https://github.com/antoinerg) | | Active, Maintainer |
|**Nicolas Kruchten** | [@nicolaskruchten](https://github.com/nicolaskruchten) | [@nicolaskruchten](https://twitter.com/nicolaskruchten) | Active, Maintainer |
|**Jon Mease** | [@jonmmease](https://github.com/jonmmease) | [@jonmmease](https://twitter.com/jonmmease) | Active |
|**Étienne Tétreault-Pinard**| [@etpinard](https://github.com/etpinard) | [@etpinard](https://twitter.com/etpinard) | Hall of Fame |
|**Mikola Lysenko**| [@mikolalysenko](https://github.com/mikolalysenko) | [@MikolaLysenko](https://twitter.com/MikolaLysenko) | Hall of Fame |
|**Ricky Reusser**| [@rreusser](https://github.com/rreusser) | [@rickyreusser](https://twitter.com/rickyreusser) | Hall of Fame |
|**Dmitry Yv.** | [@dy](https://github.com/dy) | [@DimaYv](https://twitter.com/dimayv)| Hall of Fame |
|**Robert Monfera**| [@monfera](https://github.com/monfera) | [@monfera](https://twitter.com/monfera) | Hall of Fame |
|**Robert Möstl** | [@rmoestl](https://github.com/rmoestl) | [@rmoestl](https://twitter.com/rmoestl) | Hall of Fame |
|**Nicolas Riesco**| [@n-riesco](https://github.com/n-riesco) | | Hall of Fame |
|**Miklós Tusz**| [@mdtusz](https://github.com/mdtusz) | [@mdtusz](https://twitter.com/mdtusz)| Hall of Fame |
|**Chelsea Douglas**| [@cldougl](https://github.com/cldougl) | | Hall of Fame |
|**Ben Postlethwaite**| [@bpostlethwaite](https://github.com/bpostlethwaite) | | Hall of Fame |
|**Chris Parmer**| [@chriddyp](https://github.com/chriddyp) | | Hall of Fame |
|**Alex Vados**| [@alexander-daniel](https://github.com/alexander-daniel) | | Hall of Fame |

---
## Copyright and license

Code and documentation copyright 2021 Plotly, Inc.

Code released under the [MIT license](https://github.com/plotly/plotly.js/blob/master/LICENSE).

### Versioning

This project is maintained under the [Semantic Versioning guidelines](https://semver.org/).

See the [Releases section](https://github.com/plotly/plotly.js/releases) of our GitHub project for changelogs for each release version of plotly.js.

---
## Community

* Follow [@plotlygraphs](https://twitter.com/plotlygraphs) on Twitter for the latest Plotly news.
* Implementation help may be found on community.plot.com (tagged [`plotly-js`](https://community.plotly.com/c/plotly-js)) or
  on Stack Overflow (tagged [`plotly`](https://stackoverflow.com/questions/tagged/plotly)).
* Developers should use the keyword `plotly` on packages which modify or add to the functionality of plotly.js when distributing through [npm](https://www.npmjs.com/browse/keyword/plotly).
