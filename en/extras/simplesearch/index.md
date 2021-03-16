---
title: "SimpleSearch"
_old_id: "711"
_old_uri: "revo/simplesearch"
---

## What is SimpleSearch?

SimpleSearch is a simple search component for MODX Revolution. It supports searching Resource content and TV content.

## Requirements

- MODX Revolution 2.0.0-RC-2 or later
- PHP5 or later

## History

SimpleSearch was written by [Shaun McCormick](https://github.com/splittingred) as a simple search component, and first released on June 2nd, 2010. It is loosely based on AjaxSearch for MODX Evolution by KyleJ/coroico, without the Ajax functionality.

## Upgrade risks

First of all: ALWAYS MAKE A BACKUP BEFORE UPDATING!

Upgrading to 2.0.0 from 1.\* is highly recommended, but it does introduce some risks.

Important changes from 1.\* to 2.0.0:

- The namespace has been changed from sisea to simplesearch. If you're using custom System Settings, then please migrate them.
- The ElasticSearch and SOLR drivers have been removed, because they were in need of improvements. Future drivers should be seperate addons. Feel free to ask us for help here.

### Download

It can be downloaded from within the MODX Revolution manager via [Package Management](developing-in-modx/advanced-development/package-management "Package Management"), or from the MODX Extras Repository, here: <https://modx.com/extras/package/simplesearch>

### Development and Bug Reporting

SimpleSearch is stored and developed in GitHub, and can be found here:<https://github.com/Sterc/SimpleSearch>

Bugs can be filed here: <https://github.com/Sterc/SimpleSearch/issues>

## Usage

SimpleSearch has 2 snippets - one to display a form ("SimpleSearchForm"), and the other to display search results ("SimpleSearch").

- [SimpleSearch](extras/simplesearch/simplesearch "SimpleSearch.SimpleSearch")
- [SimpleSearchForm](extras/simplesearch/simplesearch.simplesearchform "SimpleSearch.SimpleSearchForm")

## Examples

Display a search form, and below it, the results:

``` php
[[!SimpleSearchForm]]

<h2>Results</h2>
[[!SimpleSearch]]
```

Display a Search form that sends you to a results page in Resource 123 (which has the SimpleSearch call in it):

``` php
[[!SimpleSearchForm? &landing=`123`]]
```

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
