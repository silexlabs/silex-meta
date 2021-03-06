## About this meta repo

This is a [meta repository](https://github.com/mateodelnorte/meta#readme) for Silex website builder

It includes all sub projects needed for Silex development, this is the repo you need to contribute to Silex.

There is no issue on this repo, please use the individual project's issues

## Included repositories in this meta repo

| Name | Folder | Website | Description | Repo | npm | Docs | License |
|------|--------|---------|------|------|------|------|------|
| CloudExplorer | `/packages/cloud-explorer/` | [Website](https://cloud-explorer.org/) | A free customizable file browser and a self hosted node.js API server. | [Github repo](https://github.com/silexlabs/CloudExplorer2) | [npm package](https://www.npmjs.com/package/cloud-explorer) | [docs](https://github.com/silexlabs/CloudExplorer2) | |
| Prodotype | `/packages/prodotype` | [Website](http://projects.silexlabs.org/Prodotype/) | Create components and the UI to edit them out of html templates and yaml files. | [Github repo](https://github.com/silexlabs/Prodotype) | [npm package](https://www.npmjs.com/package/prodotype) | [docs](http://projects.silexlabs.org/Prodotype/) | |
| Responsize | `/packages/responsize/` | [Website](http://responsize.org/) | Display websites on different screen sizes in the browser. Useful to visualize how a website looks on desktop while browsing on mobile, or on big screen while browsing on a laptop. | [Github repo](https://github.com/silexlabs/responsize) | [npm package](https://www.npmjs.com/package/responsize) | [docs](https://github.com/silexlabs/responsize) | GPL |
| Silex templates | `/packages/silex-templates/` and `/packages/silex-blank-templates/` | [Website](https://www.silex.me/templates/) | The community templates available on [Silex Dashboard](https://github.com/silexlabs/Silex/wiki/Editor-UI#dashboard). | [Github repo](https://github.com/silexlabs/silex-templates) | [npm package](https://www.npmjs.com/package/silex-templates) | [docs](https://github.com/silexlabs/Silex/wiki/Create-templates-for-Silex) | CC |
| Silex website builder | `/packages/Silex` | [Website](https://www.silex.me) | The hackable website builder for designers. | [Github repo](https://github.com/silexlabs/Silex) | [npm package](https://www.npmjs.com/package/silex-website-builder) | [docs](https://github.com/silexlabs/Silex/wiki) | GPL and MPL |
| editor.silex.me | `/packages/editor.silex.me` | [Website](https://editor.silex.me) | Free public Silex instance hosted by Silex Labs foundation. | [Github repo](https://github.com/silexlabs/editor.silex.me) | - | [docs](https://github.com/silexlabs/Silex/wiki) | GPL |
| Silex desktop | `/packages/silex-desktop` | [Website](https://github.com/silexlabs/silex-desktop/releases/latest) | Silex desktop version, an installable application for Windows, MacOS and linux. | [Github repo](https://github.com/silexlabs/silex-desktop) | - | [docs](https://github.com/silexlabs/Silex/wiki) | GPL |
| Stage component (drag'n drop) | `/packages/drag-drop-stage-component/` | [Website](http://projects.silexlabs.org/drag-drop-stage-component/pub/) | This "stage" component enables the user select elements, drag and drop them, resize them. | [Github repo](https://github.com/silexlabs/drag-drop-stage-component) | [npm package](https://www.npmjs.com/package/drag-drop-stage-component) | [docs](https://github.com/silexlabs/drag-drop-stage-component) | MIT |
| Unifile and unifile-* | `/packages/unifile*` | [Website](http://projects.silexlabs.org/unifile/) | Nodejs library to access cloud storage services with a common API. | [Github repo](https://github.com/silexlabs/unifile) | [npm package](https://www.npmjs.com/package/unifile) | [docs](http://projects.silexlabs.org/unifile/) | MIT |

## Instructions

To contribute to Silex you need to clone this repo. 

1. As this is a meta repo, you will need to [install meta](https://github.com/mateodelnorte/meta#getting-started)
1. Clone this repo with `meta git clone git@github.com:silexlabs/silex-meta.git` or `meta git clone https://github.com/silexlabs/silex-meta.git`
1. Cd in the repo: `cd silex-meta`
1. Use the recommended version of node: `nvm use`
1. Install all dependencies: `npm install && meta exec "npm install"`
1. ~Make each project uses the development version of any other project in the meta repo: `meta npm link && meta npm link --all`~
1. Make each project uses the development version of any other project in the meta repo: `meta exec "npm link" && node scripts/link-all.js`

Useful commands

* Start Silex: `cd packages/silex-website-builder/ && npm start` (or use `npm run start:debug`)
* Release and bump version of a library and all its dependents: `meta release-version unifile`, see [Meta release plugin](https://github.com/alqh/meta-release)
* Detect which package needs a release: `node scripts/detect-changes.js`


## Third party dependencies

* [Typescript](https://www.typescriptlang.org/) is used to build Silex
* [Ace](http://ace.c9.io/), an excellent code editor in javascript
* jquery is included in the sites generated by Silex
* [GLYPHICONS library of icons and symbols](http://glyphicons.com/) ([CC license](http://creativecommons.org/licenses/by/3.0/)) and [fontawesome icons](http://fontawesome.io/)

## Size of Silex code base

This includes all the packages of this repo.

As of june 2017, around 100.000 lines of code. See [github API count (includes blank lines and comments I guess)](https://api.github.com/repos/silexlabs/Silex/languages):

```
JavaScript: 856643,
CSS: 82702,
HTML: 53727,
Shell: 1532
```

[cb372's report](http://line-count.herokuapp.com/silexlabs/Silex):

<table id="results" class="table table-striped">
<tbody>
    <tr>
        <th>File Type</th>
        <th>Files</th>
        <th>Lines of Code</th>
        <th>Total lines</th>
    </tr>
    <tr>
        <td>JavaScript</td>
        <td>422</td>
        <td>138797</td>
        <td>183644</td>
    </tr>
    <tr>
        <td>Json</td>
        <td>3</td>
        <td>146</td>
        <td>146</td>
    </tr>
    <tr>
        <td>Text</td>
        <td>12</td>
        <td>0</td>
        <td>1047</td>
    </tr>
    <tr>
        <td>Shell</td>
        <td>4</td>
        <td>24</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Stylesheets</td>
        <td>90</td>
        <td>17777</td>
        <td>21504</td>
    </tr>
    <tr>
        <td>Html</td>
        <td>7</td>
        <td>545</td>
        <td>726</td>
    </tr>
</tbody>
</table>


[Cloc's report](https://github.com/AlDanial/cloc) in mar. 2021:

```
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JavaScript                     149           9652          10733          54582
JSON                            55              3              0          52723
TypeScript                     178           2591           4713          21524
HTML                           114          16988            380          16689
CSS                             57           2142           1098          14399
SCSS                            57            881            415           5444
SVG                             17              0              0           4810
LESS                            36            172            203           4039
YAML                            38             18             46           2607
EJS                             28             40              9           1627
JSX                             14            160            109           1406
Markdown                        42            472              0           1067
Pug                             17             54             36            938
Dockerfile                       1              3              3              9
Properties                       1              1              0              1
-------------------------------------------------------------------------------
SUM:                           804          33177          17745         181865
-------------------------------------------------------------------------------
```


