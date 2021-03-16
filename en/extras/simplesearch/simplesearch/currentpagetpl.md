---
title: "currentPageTpl"
_old_id: "999"
_old_uri: "revo/simplesearch/simplesearch.simplesearch/simplesearch.simplesearch.currentpagetpl"
---

## SimpleSearch's currentPageTpl Chunk

This is the Chunk displayed with the &currentPageTpl property on the [SimpleSearch](extras/simplesearch/simplesearch "SimpleSearch.SimpleSearch") snippet. It contains a simple, active, unclickable pagination link.

## Default Value

``` php
<span class="sisea-page sisea-current-page">[[+text]]</span>
```

## Available Placeholders

| Name      | Description                         |
| --------- | ----------------------------------- |
| text      | The text, or number, of each page.  |
| separator | The separator between page numbers. |
| link      | The same as the text property.      |

## See Also

1. [SimpleSearch.SimpleSearch](extras/simplesearch/simplesearch)
    1. [SimpleSearch.SimpleSearch.containerTpl](extras/simplesearch/simplesearch/containertpl)
    2. [SimpleSearch.SimpleSearch.currentPageTpl](extras/simplesearch/simplesearch/currentpagetpl)
    3. [SimpleSearch.SimpleSearch.pageTpl](extras/simplesearch/simplesearch/pagetpl)
    4. [SimpleSearch.SimpleSearch.tpl](extras/simplesearch/simplesearch/tpl)
    5. [SimpleSearch.Faceted Search Through PostHooks](extras/simplesearch/simplesearch/faceted-search-through-posthooks)
2. [SimpleSearch.SimpleSearchForm](extras/simplesearch/simplesearch.simplesearchform)
    1. [SimpleSearch.SimpleSearchForm.tpl](extras/simplesearch/simplesearch.simplesearchform/tpl)
3. [SimpleSearch.Solr](extras/simplesearch/simplesearch.solr)
