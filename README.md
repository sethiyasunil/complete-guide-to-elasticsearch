# readme
This repository contains all of the queries used within the [Complete Guide to Elasticsearch course](https://l.codingexplained.com/course/elasticsearch?src=github).


## key terms

```
Elastic Stack
Kibana: Visualization platform for elastic search.
LogStash: Data processing pipeline - log file enteries, orders, chat events etc.
	LogStacsh pipeline consit of Input,Process and outputs
XPack:  Adds additional functionality to Kibana - e.g. Security, authentication and authorisation, monitoring e.g. cup, ram usage, alerting, reporting, Graph
Beats- collection of data shippers. Collect data and share to logstash or xpack.  e.g. FileBeats (processl logs and sent to ES).
Cluster - collection of nodes
Node - is an instance of elastic search. Each instance is Lucene Search.
Indices - collection of documents
Document - data is stored in documents as json files.
Shard- Sharding is a way to divide an index into peices. Each peice is called shard. Sharding gives horiziontal scaling.
USe split and shrink API to add or reduce the number of shared.
Replication - copies of shard. Copy is not maintained on same node.
Nodes Types (or Roles) - master, data, injest, machine learning, coordination
Adpative Replica Selection - ES select one of the shared from shard group ( primary or replica) to handle requests.

ES retain version number of deleted document for  60 sec. Version number is incremented if you upload a document with same id within 60 seconds. Otherwise it reset version number to 1.
Version is not used for optimistic locking. Primary term and sequence_no is used for optimistic locking.

Batch processing  (/products/_bulk) - operations allowed a) index b)create c) update d) delete  
index - create or update document. It always succees
create - fails if document already exist


Fields : _index, _id, _source, _version,


dynamic - true,false,strict
	true - enable dynamic mapping
	false - new fields are ignored
	strict - ES throw an exception when see unknown field.
	
	
Analyser - Character Token filters  + 	Tokeniser + Token Filters
Character filters -e.g. html_strip, pattern_replace
Tokeniser e.g. standardtokeniser, letter tokeniser, lowercase tokeniser, whitespacetokeiser, ngram tokeniser
Token Filters: standard (does nothing), uppercase, stopwords, word_dlimiter ( e.g. WiFi, wi-Fi), stemmer ( running to run), synonyms
Analyser -
e.g. simple, stop, pattern, whitespace, standard

standard analyzer comprises of  * No character token filter + Standardard Tokeniser + standard token filter
Standardard Tokeniser removes simples (e.g. -) and tokenise with whitespaces.
standard token filter  comprises of lowercase token filter + stopwords token filter


query context /filter context : Query context effect reqults score. Filter context doesn't effect context score.


proximity-searches : search words with 'match_phrase clause and slop. It search words even if other words are in between them(proximity).
"fuzziness": "auto" : search even when typo in input.

```

## Getting Started

```
inspecting-the-cluster.md
sending-queries-with-curl.md
sharding-and-scalability.md
understanding-replication.md
adding-more-nodes-to-the-cluster-for-development.md
overview-of-node-roles.md
```

## Managing Documents

```
creating-and-deleting-indices.md
indexing-documents.md
retrieving-documents-by-id.md
updating-documents.md
scripted-updates.md
upserts.md
replacing-documents.md
deleting-documents.md
optimistic-concurrency-control.md
update-by-query.md
delete-by-query.md
batch-processing.md
importing-data-with-curl.md
```

## Mapping

```
dynamic-mapping.md
adding-mappings-to-existing-indices.md
changing-existing-mappings.md
adding-multi-fields-mappings.md
defining-custom-date-formats.md
picking-up-new-fields-without-dynamic-mapping.md
```

## Analysis & Analyzers

```
using-the-analyze-api.md
configuring-built-in-analyzers.md
creating-custom-analyzers.md
using-analyzers-in-mappings.md
```

## Introduction to Searching

```
searching-with-the-request-uri.md
introducing-the-query-dsl.md
understanding-relevance-scores.md
debugging-unexpected-query-results.md
full-text-queries-vs-term-level-queries.md

```

## Term Level Queries

```
searching-for-a-term.md
searching-for-multiple-terms.md
retrieving-documents-based-on-ids.md
matching-documents-with-range-values.md
working-with-relative-dates.md
matching-documents-with-non-null-values.md
matching-based-on-prefixes.md
searching-with-wildcards.md
searching-with-regular-expressions.md
exercises.md
```

## Full Text Queries

```
introduction-to-full-text-queries.md
flexible-matching-with-match-query.md
matching-phrases.md
searching-multiple-fields.md
exercises.md
```

## Adding Boolean Logic to Queries

```
debugging-bool-queries-with-named-queries.md
how-the-match-query-works.md
querying-with-boolean-logic.md
```

## Joining Queries

```
querying-nested-objects.md
nested-inner-hits.md
mapping-document-relationships.md
adding-documents.md
querying-by-parent-id.md
querying-child-documents-by-parent.md
querying-parent-by-child-documents.md
multi-level-relations.md
parent-child-inner-hits.md
terms-lookup-mechanism.md
```

## Controlling Query Results

```
specifying-the-result-format.md
source-filtering.md
specifying-the-result-size.md
specifying-an-offset.md
sorting-results.md
sorting-by-multi-value-fields.md
filters.md
```

##  Aggregations

```
introduction-to-aggregations.md
metric-aggregations.md
introduction-to-bucket-aggregations.md
nested-aggregations.md
filtering-out-documents.md
defining-bucket-rules-with-filters.md
range-aggregations.md
histograms.md
global-aggregation.md
missing-field-values.md
aggregating-nested-objects.md


```

## Improving Search Results

```
proximity-searches.md
affecting-relevance-scoring-with-proximity.md
fuzzy-match-query.md
fuzzy-query.md
adding-synonyms.md
adding-synonyms-from-file.md
highlighting-matches-in-fields.md
stemming.md
```








