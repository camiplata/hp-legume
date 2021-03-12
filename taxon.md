---
title: Taxon
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

<div id="taxon"></div>

<script>
'use strict';
const e = React.createElement;
class Taxon extends React.Component {

    render() {

      return e(
        ColBrowser.Taxon,
        { catalogueKey: 9999,
          pathToTree: '/browse',
          pathToSearch= '/data/search',
          pathToDataset: '/sourcedatasets/',
          pathToTaxon: '/taxon/' 
          pageTitleTemplate: 'COL | __taxon__'}
      );
    }
  }

const domContainer = document.querySelector('#taxon');
ReactDOM.render(e(Taxon), domContainer);
</script>
