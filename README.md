# A Brief Review of Hyperparameter Optimization Methods for Machine Learning

Richard Wen  
rrwen.dev@gmail.com  

* [Slides](https://rrwen.github.io/slides-rmcs-litreview)
* [PDF](https://github.com/rrwen/slides-rmcs-litreview/blob/master/slides/wen2017_hyperoptml_slides.pdf)
* [Paper](https://github.com/rrwen/assign-rmcs-litreview)

Presentation slides for Research Methods in Computer Science Course Instructed by Dr. Cherie Ding.

[![Build Status](https://travis-ci.org/rrwen/slides-rmcs-litreview.svg?branch=master)](https://travis-ci.org/rrwen/slides-rmcs-litreview)
[![GitHub license](https://img.shields.io/github/license/rrwen/slides-rmcs-litreview.svg)](https://github.com/rrwen/slides-rmcs-litreview/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/rrwen/slides-rmcs-litreview.svg?style=social)](https://twitter.com/intent/tweet?text=Presentation%20slides%20for%20Research%20Methods%20in%20Computer%20Science%20Course%20Instructed%20by%20Dr.%20Cherie%20Ding.:%20https%3A%2F%2Fgithub.com%2Frrwen%2Fslides-rmcs-litreview%20%23revealjs%20%23slides)

## Developer Notes

### Generate Slides

1. Install [npm](https://www.npmjs.com/)
2. [Clone](https://git-scm.com/docs/git-clone) this repository
3. Generate `docs/index.html` (see `script.html`) in [package.json](https://github.com/rrwen/slides-rmcs-litreview/blob/master/package.json)
4. Generate `slides/wen2017_hyperoptml_slides.pdf` (see `script.pdf`) in [package.json](https://github.com/rrwen/slides-rmcs-litreview/blob/master/package.json)

```
git clone https://github.com/rrwen/slides-rmcs-litreview
cd slides-rmcs-litreview
npm install
npm run html
npm run pdf
```

### Edits

The following can be edited before generating:

* `slides/wen2017_hyperoptml_slides.md`: [Markdown](https://daringfireball.net/projects/markdown/) file with slide contents
* `slides/template.html`: [Custom reveal-md template](https://github.com/webpro/reveal-md#custom-template) 
* `docs/edit/style.css`: [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) file to adjust styling of slides
* `docs/edit/logo.png`: logo image to use

### Implementation


The slides [slides-rmcs-litreview](https://github.com/rrwen/slides-rmcs-litreview) uses the following [npm](https://www.npmjs.com/) packages for its implementation:

npm | Purpose
--- | ---
[reveal-md](https://www.npmjs.com/package/reveal-md) | Converting `slides/wen2017_hyperoptml_slides.md` markdown to `docs/index.html` reveal html slides
[decktape](https://www.npmjs.com/package/decktape) | Converting `slides/wen2017_hyperoptml_slides.md` markdown to `slides/wen2017_hyperoptml_slides.pdf` format 
[windows-build-tools](https://www.npmjs.com/package/windows-build-tools) | Compiling dependencies for decktape on Windows Operating System (OS)

```
       reveal-md            <-- Convert markdown  slides to html

       decktape             <-- Convert markdown slides to pdf
          |
  windows-build-tools       <-- Compile decktape on Windows OS
```
