---
title: Taxon
permalink: /taxonomy/taxon
layout: documentation
sideNavigation: sidenav.taxonomy
head: |
   <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.7.8/umd/main.css">
---

<!--react and gbif component-->
<script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>

<script src="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.7.8/umd/col-browser.min.js" ></script>

<div id="taxon"></div>

<script>
'use strict';
const e = React.createElement;
class Taxon extends React.Component {

    render() {

      return e(
        ColBrowser.Taxon,
        { 
          catalogueKey: 2232,
          pathToTree: '/taxonomy/browse',
          pathToSearch: '/taxonomy/search',
          pathToTaxon: '/taxonomy/taxon/',
          pathToDataset: '/sourcedatasets/',
          pageTitleTemplate: 'Legume | __taxon__'
        }
      );
    }
  }

const domContainer = document.querySelector('#taxon');
ReactDOM.render(e(Taxon), domContainer);
</script>
