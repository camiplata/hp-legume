---
title: Browse
description: Lorem markdownum spatium limes indefessus neque at orat aestuat
background: https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Haeckel_Caulerpa_paspaloides.JPG/1024px-Haeckel_Caulerpa_paspaloides.JPG
imageLicense: Kunstformen der Natur (1904) by Ernst Haeckel via [Wikimedia](https://commons.wikimedia.org/wiki/Kunstformen_der_Natur)
overlayColor: "#00000055"
parallax: true
height: 50vh
layout: post
head: |
   <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.4.6/umd/main.css">
---

<!--react and gbif component-->
<script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>

<script src="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.4.6/umd/col-browser.min.js" ></script>

<div id="tree"></div>

<script>
'use strict';
const e = React.createElement;
class Tree extends React.Component {

    render() {

      return e(
        ColBrowser.Tree,
        { catalogueKey: 2232,
          pathToTaxon: '/taxon/',
          defaultTaxonKey: 'x3YN'
        }
      );
    }
  }

const domContainer = document.querySelector('#tree');
ReactDOM.render(e(Tree), domContainer);
</script>
