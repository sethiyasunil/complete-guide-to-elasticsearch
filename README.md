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

##

```
```

##
```
```

##

```
```


Adding Boolean Logic to Queries\debugging-bool-queries-with-named-queries.md
Adding Boolean Logic to Queries\how-the-match-query-works.md
Adding Boolean Logic to Queries\querying-with-boolean-logic.md
Aggregations\aggregating-nested-objects.md
Aggregations\defining-bucket-rules-with-filters.md
Aggregations\filtering-out-documents.md
Aggregations\global-aggregation.md
Aggregations\histograms.md
Aggregations\introduction-to-aggregations.md
Aggregations\introduction-to-bucket-aggregations.md
Aggregations\metric-aggregations.md
Aggregations\missing-field-values.md
Aggregations\nested-aggregations.md
Aggregations\range-aggregations.md
Analysis & Analyzers\configuring-built-in-analyzers.md
Analysis & Analyzers\creating-custom-analyzers.md
Analysis & Analyzers\using-analyzers-in-mappings.md
Analysis & Analyzers\using-the-analyze-api.md
Controlling Query Results\filters.md
Controlling Query Results\sorting-by-multi-value-fields.md
Controlling Query Results\sorting-results.md
Controlling Query Results\source-filtering.md
Controlling Query Results\specifying-an-offset.md
Controlling Query Results\specifying-the-result-format.md
Controlling Query Results\specifying-the-result-size.md
Full Text Queries\exercises.md
Full Text Queries\flexible-matching-with-match-query.md
Full Text Queries\introduction-to-full-text-queries.md
Full Text Queries\matching-phrases.md
Full Text Queries\searching-multiple-fields.md
Improving Search Results\adding-synonyms-from-file.md
Improving Search Results\adding-synonyms.md
Improving Search Results\affecting-relevance-scoring-with-proximity.md
Improving Search Results\fuzzy-match-query.md
Improving Search Results\fuzzy-query.md
Improving Search Results\highlighting-matches-in-fields.md
Improving Search Results\proximity-searches.md
Improving Search Results\stemming.md
Introduction to Searching\debugging-unexpected-query-results.md
Introduction to Searching\full-text-queries-vs-term-level-queries.md
Introduction to Searching\introducing-the-query-dsl.md
Introduction to Searching\searching-with-the-request-uri.md
Introduction to Searching\understanding-relevance-scores.md
Joining Queries\adding-documents.md
Joining Queries\mapping-document-relationships.md
Joining Queries\multi-level-relations.md
Joining Queries\nested-inner-hits.md
Joining Queries\parent-child-inner-hits.md
Joining Queries\querying-by-parent-id.md
Joining Queries\querying-child-documents-by-parent.md
Joining Queries\querying-nested-objects.md
Joining Queries\querying-parent-by-child-documents.md
Joining Queries\terms-lookup-mechanism.md
Mapping\adding-mappings-to-existing-indices.md
Mapping\adding-multi-fields-mappings.md
Mapping\changing-existing-mappings.md
Mapping\defining-custom-date-formats.md
Mapping\dynamic-mapping.md
Mapping\picking-up-new-fields-without-dynamic-mapping.md
Term Level Queries\exercises.md
Term Level Queries\matching-based-on-prefixes.md
Term Level Queries\matching-documents-with-non-null-values.md
Term Level Queries\matching-documents-with-range-values.md
Term Level Queries\retrieving-documents-based-on-ids.md
Term Level Queries\searching-for-a-term.md
Term Level Queries\searching-for-multiple-terms.md
Term Level Queries\searching-with-regular-expressions.md
Term Level Queries\searching-with-wildcards.md
Term Level Queries\working-with-relative-dates.md
