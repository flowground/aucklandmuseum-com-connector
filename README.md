# ![LOGO](logo.png) Auckland Museum **flow**ground Connector

## Description

A generated **flow**ground connector for the Auckland Museum API (version 2.0.0).

Generated from: https://api.apis.guru/v2/specs/aucklandmuseum.com/2.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:37:02+03:00

## API Description

This is technical documentation for the Auckland Museum API


## Authorization

This API does not require authorization.

## Actions

### Retrieve media associated with Collections and Cenotaph subjects in Auckland Museum

> Gets `media` at a given path

*Tags:* `media`

#### Input Parameters
* `path` - _required_ - The media `identifier`

* `rendering` - _optional_ - The desired media `rendering`

Possible values:
* `original.jpg`
* `original.pdf`
* `thumbnail.jpg` (fixed with 70px)
* `standard.jpg` (fixed width 440px and height 440px)
* `preview.jpg` (fixed height 100px)


### Explore details about a given subject node

> Gets information about a `subject` identified by the `identifier`.<br/>
> <br/>
> The response format depends upon the `Accept` header.<br/>
>   - `text/html` - the default response type. Returned data can be easily viewed in any modern Internet Browser<br/>
>   - `application/ld+json` - the response will be in [JSON-LD](http://json-ld.org/)<br/>
>   - `application/json` - the response will be a simple JSON Object with keys (predicates) and values (objects).

*Tags:* `subject`

#### Input Parameters
* `identifier` - _required_ - The identifier path of the `subject` you're looking for


### Perform simple search queries over Auckland Museum Collections and Cenotaph data

> Use this endpoint to perform simple search queries for finding information and subjects you may be interested in<br/>
> <br/>
> Searches performed via this endpoint run against an [Elastic](www.elastic.co) server. This endpoint mirrors the Elastic search API documented [here](https://www.elastic.co/guide/en/elasticsearch/reference/1.5/search-search.html)<br/>
> <br/>
> Use the<br/>
>   - `collectionsonline` index to perform searches over other all<br/>
> Collections data<br/>
>   - `cenotaph` index to perform searches over Cenotaph data

*Tags:* `search`

#### Input Parameters
* `index` - _required_ - search index name
Possible values:
* `collectionsonline`
* `cenotaph`

* `operation` - _required_ - One of the supported elasticsearch operations like `_search` or `_suggest`
* `q` - _optional_ - One of the supported elasticsearch query parameter values for key `q`

### Perform complex search queries over Auckland Museum Collections and Cenotaph data

> Searches performed via this endpoint run against an [Elastic](www.elastic.co) server. This endpoint mirrors the Elastic search API documented [here](https://www.elastic.co/guide/en/elasticsearch/reference/1.5/search-search.html)<br/>
> <br/>
> Use the<br/>
>   - `collectionsonline` index to perform searches over other all Collections data<br/>
>   - `cenotaph` index to perform searches over Cenotaph data

*Tags:* `search`

#### Input Parameters
* `index` - _required_ - search index name
Possible values:
* `collectionsonline`
* `cenotaph`

* `operation` - _required_ - One of the supported elasticsearch operations like `_search` or `_suggest`

### Auckland Museum SPARQL endpoint

> You can execute your [SPARQL](http://www.w3.org/TR/rdf-sparql-query/) queries against this endpoint.<br/>
> <br/>
> The sparql query should be provided as the value of the request parameter `query`.<br/>
> Set the `Accept` header to `application/sparql-results+xml` to get results in XML. Set it to `application/sparql-results+json` to get results in JSON. <br/>
> <br/>
> **Note:** This endpoints supports [JSON-P](http://json-p.org/). In order to get a JSON-P response, set the query parameter `callback` to your preferred callback function name. The default function name is `callback()`. When using JSON-P, there is no need to set the `Accept` header because the response will always be in `application/javascript`.

*Tags:* `sparql`

#### Input Parameters
* `query` - _required_ - sparql query
* `callback` - _optional_ - The [JSON-P](http://json-p.org/) callback parameter
* `infer` - _optional_ - Whether to get inferred results in the response

### Auckland Museum SPARQL endpoint

> You can execute your [SPARQL](http://www.w3.org/TR/rdf-sparql-query/) queries against this endpoint.<br/>
> The sparql query should be provided as the value of the request parameter `query`.<br/>
> Set the `Accept` header to `application/sparql-results+xml` to get results in XML. Set it to `application/sparql-results+json` to get results in JSON.

*Tags:* `sparql`

## License

**flow**ground :- Telekom iPaaS / aucklandmuseum-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
