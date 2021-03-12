---
title: Taxon
permalink: /taxonomy/search
description: Lorem markdownum spatium limes indefessus neque at orat aestuat
layout: documentation
sideNavigation: sidenav.taxonomy
klass: fullwidth
head: |
   <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.7.8/umd/main.css">
---

<!--react and gbif component-->
<script src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>

<script src="https://cdn.jsdelivr.net/gh/CatalogueOfLife/portal-components@0.7.8/umd/col-browser.min.js" ></script>

## Acknowledgements
TODO: give credit somewhere. Here for example.

<div id="search"></div>

<script >
'use strict';
const e = React.createElement;
class Search extends React.Component {

    render() {

      return e(
        ColBrowser.Search,
        { 
          catalogueKey: 2232,
          pathToTree: '/taxonomy/browse',
          pathToSearch: '/taxonomy/search',
          pathToTaxon: '/taxonomy/taxon/'  
        }
      );
    }
  }

const domContainer = document.querySelector('#search');
ReactDOM.render(e(Search), domContainer);
</script>
