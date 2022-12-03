![SWIRL Logo](https://raw.githubusercontent.com/sidprobstein/swirl-search/main/docs/images/swirl_logo_1024.jpg)

# SWIRL FEDERATED SEARCH ENGINE

SWIRL is the first open source, [Federated Search Engine](https://en.wikipedia.org/wiki/Federated_search)! 

SWIRL makes it easy for search developers, data scientists and power users to query multiple search engine silos at once and quickly receive unified results *without* extracting and indexing *anything*. It includes connectors to elastic, solr, Google PSE, NLResearch.com, generic HTTP/GET/JSON and Sqlite3 that are easy to configure, without writing code. Then use SWIRL's simple REST APIs to run searches and quickly retrieve unified results, re-ranked by SWIRL using built-in cosine-vector similarity plus term and phrase boosts.

SWIRL is available under the [Apache 2.0 license](https://github.com/sidprobstein/swirl-search/blob/main/LICENSE), and leans heavily on the popular python/django/celery/rabbit-mq stack - a universe of plug-ins that can extend and integrate SWIRL with a range of existing systems.

<br/>

# Releases

| Version                     | Date                        | Notes | 
| --------------------------- | --------------------------- | ----- |
| [SWIRL SEARCH 1.7](https://github.com/sidprobstein/swirl-search/releases/tag/v1.7) | 12-3-2022 | [Release 1.7](./docs/RELEASE_NOTES_1.7.md) |
| [Docker Image](https://hub.docker.com/r/sidprobstein/swirl-search) | * | [Setup Guide](https://github.com/sidprobstein/swirl-search/wiki/1.-Quick-Start#docker) - Note, not for production use, *does* *not* *persist* *data* after shutdown! | 

<br/>

# Screen Shots

### Google PSE Search Providers
![SWIRL SearchProviders](https://raw.githubusercontent.com/sidprobstein/swirl-search/main/docs/images/swirl_providers_focus.png)

### Relevancy Ranked Results
![SWIRL Results](https://raw.githubusercontent.com/sidprobstein/swirl-search/main/docs/images/swirl_results_focus.png)

<br/>

# Features

* [Pre-built searchprovider definitions](https://github.com/sidprobstein/swirl-search/tree/main/SearchProviders) for apache solr, elastic, Sqlite3, PostgreSQL, generic http/get/auth/json and pay services like NLResearch.com and Newsdata.io that are configured, NOT coded, and are easily [organized with properties and tags](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#organizing-searchproviders-with-active-default-and-tags)

* [Adaptation of the query for each provider](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#search-syntax) such as rewriting ```NOT term``` to ```-term```, removing NOTted terms from providers that don't support NOT, and passing down AND, + and OR.

* [Synchronous or asynchronous search federation](https://github.com/sidprobstein/swirl-search/wiki/3.-Developer-Guide#architecture) via [REST APIs](http://localhost:8000/swirl/swagger-ui/)

* Data landed in Sqlite3 or PostgreSQL for post-processing, consumption and analytics

* [Matching on word stems](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#relevancy) and [handling of stopword](https://github.com/sidprobstein/swirl-search/wiki/4.-Object-Reference#stopwords-language) via NLTK

* Re-ranking of unified results [using Cosine Vector Similarity](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#relevancy) based on [spaCy](https://spacy.io/)'s large language model and [NLTK](https://www.nltk.org/)

* [Result mixers](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#result-mixers) operate on landed results and order results by relevancy, date, stack or round-robin

* Sort results by provider date, relevancy or stack/round robin to get a cross-section of the best results from all providers

* Page through all results requested, re-run and re-score searches using URLs provided in each result set

* [Sample data sets](https://github.com/sidprobstein/swirl-search/tree/main/Data) for use with Sqlite3 and PostgreSQL

* [Optional spell correction](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide#spell-correction) using TextBlob

* [Optional search/result expiration service](https://github.com/sidprobstein/swirl-search/wiki/5.-Admin-Guide#search-expiration-service) to limit storage use

* Easily extensible [Connector](https://github.com/sidprobstein/swirl-search/tree/main/swirl/connectors) and [Mixer](https://github.com/sidprobstein/swirl-search/tree/main/swirl/mixers) objects

* [Available under the Apache 2.0 License](./LICENSE)

<br/>

# Documentation

* [Home](https://github.com/sidprobstein/swirl-search/wiki)
* [Quick Start](https://github.com/sidprobstein/swirl-search/wiki/1.-Quick-Start)
* [User Guide](https://github.com/sidprobstein/swirl-search/wiki/2.-User-Guide)
* [Developer Guide](https://github.com/sidprobstein/swirl-search/wiki/3.-Developer-Guide)
* [Object Reference](https://github.com/sidprobstein/swirl-search/wiki/4.-Object-Reference)
* [Admin Guide](https://github.com/sidprobstein/swirl-search/wiki/5.-Admin-Guide)

<br/>

# Contributing

* Review the [help wanted list](docs/help_wanted.md)

* Submit a [pull request](https://github.com/sidprobstein/swirl-search/pulls) with changes

<br/>

# Support

:small_blue_diamond: [Create an Issue](https://github.com/sidprobstein/swirl-search/issues) if something doesn't work, isn't clear, or should be documented

:small_blue_diamond: Email: [support@swirl.today](mailto:support@swirl.today) with issues, requests, questions, etc - we'd love to hear from you!

<br/>



