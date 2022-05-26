Clojure graph resources
=======================
This is a curated list of mostly mature and/or actively developed Clojure resources relevant for dealing with graph-like data. It's currently being expanded as I explore this area more thoroughly. Suggestions are welcome in the form of pull requests or Github issues. I try to steer around abandonware, though.

> If you're interested in DSLs and parsing, be sure to check out [clojure-dsl-resources](https://github.com/simongray/clojure-dsl-resources) too.

Data structures / algorithms
----------------------------
* [aysylu/loom](https://github.com/aysylu/loom): Graph library for Clojure.
* [Engelberg/ubergraph](https://github.com/Engelberg/ubergraph): An all-purpose Clojure graph data structure that implements Loom protocols and more.
* [ont-app/igraph](https://github.com/ont-app/igraph): IGraph defines a protocol which aims to provide a general interface to a variety of graph-based representations.
* [totakke/jungerer](https://github.com/totakke/jungerer): Clojure network/graph library wrapping JUNG.
* [pangloss/fermor](https://github.com/pangloss/fermor): Fast, powerful, general-purpose graph traversal and modelling tools plus a performant immutable in-memory graph database.
* [ekoontz/dag-unify](https://github.com/ekoontz/dag-unify): A Clojure library for combining directed acyclic graphs (DAGs) via unification.
* [aroemers/rmap](https://github.com/aroemers/rmap): Clojure library for defining recursive maps; literally, programmatically and with pure data.
* [cjsauer/joinery](https://github.com/cjsauer/joinery): Enables traversal of in-memory graph-like data structures using Clojure(Script)'s map protocols.

Visualisation
-------------
* [chrismurrph/show-graph](https://github.com/chrismurrph/show-graph): Translates a particular directed graph data structure (graph with vertices and edges) into a JavaFX view that can be seen from Reveal.
* [jebberjeb/specviz](https://github.com/jebberjeb/specviz): Generate Graphviz images from clojure.spec.
* [benedekfazekas/morpheus](https://github.com/benedekfazekas/morpheus): Generate dependency graph(s) for variables in Clojure(Script) namespaces.
* [jpmonettas/clograms](https://github.com/jpmonettas/clograms): Clojure[Script] source code diagrams.
* [jafingerhut/cljol](https://github.com/jafingerhut/cljol): Visualise the memory usage of a Java object and all the objects that it references as a graph.

Databases
---------
### Labeled-property graph
Labeled-property graph databases use complex graph models where edges and vertices can have both labels and associated properties.

* [gorillalabs/neo4j-clj](https://github.com/gorillalabs/neo4j-clj): Clojuresque client to Neo4j database, based upon the bolt protocol.
* [full-spectrum/neo4clj](https://github.com/full-spectrum/neo4clj): Neo4clj is a idomatic clojure client, exclusivly using Bolt for performance.         

### RDF + OWL
RDF triplestores are a specialised type of graph database for representing knowledge graphs; part of the W3C Semantic Web standards.

* [arachne-framework/aristotle](https://github.com/arachne-framework/aristotle): An RDF/OWL library for Clojure, providing a data-oriented wrapper for Apache Jena.
  - [ont-app/igraph-jena](https://github.com/ont-app/igraph-jena): This is a port of the Jena APIs to the IGraph protocol.
* [Swirrl/grafter](https://github.com/Swirrl/grafter): Linked Data & RDF Manufacturing Tools in Clojure.
  - [Swirrl/matcha](https://github.com/Swirrl/matcha) In-memory, schemaless triplestore with a SPARQL-like DSL.
  - [ont-app/igraph-grafter](https://github.com/ont-app/igraph-grafter): A port of the IGraph protocols to the Grafter protocols.
* [stardog-union/stardog-clj](https://github.com/stardog-union/stardog-clj): Clojure language bindings for the proprietary Stardog Graph / RDF Database.
* [fluree/db](https://github.com/fluree/db): Fluree is an immutable, temporal, ledger-backed semantic graph database that has a cloud-native architecture.
* [fluree/json-ld](https://github.com/fluree/json-ld): A Clojure(script) JSON-LD library.
* [yetanalytics/flint](https://github.com/yetanalytics/flint): A Clojure(Script) DSL for creating SPARQL query and update strings.
* [Swirrl/csv2rdf](https://github.com/Swirrl/csv2rdf): Clojure library and application implementing the [W3C CSV on the Web tabular metadata specifications](https://w3c.github.io/csvw/) for converting CSV to RDF.
* [ont-app/vocabulary](https://github.com/ont-app/vocabulary): Utilities to map between clojure namespaced keywords and RDF-style URIs.
* [phillord/tawny-owl](https://github.com/phillord/tawny-owl): Tawny-OWL allows construction of OWL ontologies, in a evaluative, functional and fully programmatic environment.
  - [phillord/owl-primer](https://github.com/phillord/owl-primer): The Ontology from the owl-primer written using Tawny-OWL.
* [sam_russell/porta-owl-sqwrl](https://gitlab.com/sam_russell/porta-owl-sqwrl): (GITLAB) A Clojure domain-specific language for Web Ontology Language (OWL) and Semantic (Query) Web Rule Language (SQWRL).

### Datalog
Clojure's Datomic-like databases also model data as triplets... or in some cases technically as quintuplets AKA datoms. See [clojurelog.github.io](https://clojurelog.github.io/) for a comparison of some of the Datalog database options listed below.

* [Datomic.com](https://www.datomic.com/): _(PROPRIETARY)_ A transactional database with a flexible data model, elastic scaling, and rich queries.
  - [vvvvalvalval/datofu](https://github.com/vvvvalvalval/datofu): This library provides common utilities for working with Datomic, mostly in the form of database functions.
  - [vvvvalvalval/datomock](https://github.com/vvvvalvalval/datomock): Mocking and forking Datomic Peer connections in-memory.
  - [vvvvalvalval/datalog-rules](https://github.com/vvvvalvalval/datalog-rules): Utilities for managing Datalog rulesets from Clojure.
  - [avescodes/conformity](https://github.com/avescodes/conformity): A Clojure/Datomic library for idempotently transacting norms into your database.
  - [JarrodCTaylor/schema-cartographer](https://github.com/JarrodCTaylor/schema-cartographer): Schema Cartographer provides a means to visualize, navigate, create, edit and share the relationships that exist in your Datomic schema.
  - [Provisdom/spectomic](https://github.com/Provisdom/spectomic): Generate Datomic or Datascript schema from your Clojure(script) specs.
  - [ivarref/gen-fn](https://github.com/ivarref/gen-fn): Generate Datomic function literals from regular Clojure namespaces (on-prem).
  - [ivarref/rewriting-history](https://github.com/ivarref/rewriting-history): A library to rewrite Datomic history (on-prem).
  - [ivarref/yoltq](https://github.com/ivarref/yoltq): An opinionated Datomic queue for building more reliable systems (on-prem).
  - [ivarref/double-trouble](https://github.com/ivarref/double-trouble): Handle duplicate Datomic transactions with ease.
  - [ivarref/datomic-schema](https://github.com/ivarref/datomic-schema): Simplified writing of Datomic schemas.
  - [ont-app/datomic-client](https://github.com/ont-app/datomic-client): Ports the Datomic Client to the IGraph protocols.
* [tonsky/datascript](https://github.com/tonsky/datascript): An immutable in-memory database and Datalog query engine in Clojure and ClojureScript.
  - [mpdairy/posh](https://github.com/mpdairy/posh): Posh is a ClojureScript / React library that lets you use a single DataScript database to store your app state.
  - [denistakeda/re-posh](https://github.com/denistakeda/re-posh): Re-posh allows Posh and re-frame to work together by adding support for re-frame specific subscriptions, events, effects, and co-effects to Posh.
  - [metasoarous/datsync](https://github.com/metasoarous/datsync): This library offers tools for building DataScript databases as materialized views (very much in the re-frame/samsa sense) of some master/central Datomic database.
  - [frankiesardo/minikusari](https://github.com/frankiesardo/minikusari): minikusari is a minimal rule engine built on top of Datascript (and can work with Datomic or Datahike).
  - [ont-app/datascript-graph](https://github.com/ont-app/datascript-graph): An implementation of the IGraph protocol extended to datascript.
* [mhuebert/re-db](https://github.com/mhuebert/re-db): Attempts to be a fast, reactive, client-side triple-store for handling global state in ClojureScript apps, inspired by Datomic/DataScript, working in conjunction with Reagent.
* [replikativ/datahike](https://github.com/replikativ/datahike): Datahike is a durable Datalog database powered by an efficient Datalog query engine.
  - [replikativ/datahike-frontend](https://github.com/replikativ/datahike-frontend): A front-end to Datahike written in Fulcro.
  - [lambdaforge/datalog-parser](https://github.com/lambdaforge/datalog-parser): This parser is used by Datahike and follows the Datalog dialect of Datomic.
* [juji-io/datalevin](https://github.com/juji-io/datalevin): Datalevin is a simple durable Datalog database.
* [quoll/asami](https://github.com/quoll/asami): A graph database, for Clojure and ClojureScript.
  - [quoll/asami-loom](https://github.com/quoll/asami-loom): This library extends Asami in-memory graphs to Loom.
* [xtdb/xtdb](https://github.com/xtdb/xtdb): XTDB is a general purpose database with graph-oriented bitemporal indexes.
* [Workiva/eva](https://github.com/Workiva/eva): Eva is a distributed database-system implementing an entity-attribute-value data-model that is time-aware, accumulative, and atomically consistent.
* [ribelo/doxa](https://github.com/ribelo/doxa/): An in-memory datalog database implemented with [Meander](https://github.com/noprompt/meander).
* [threatgrid/naga](https://github.com/threatgrid/naga): Datalog based rules engine.
* [den1k/nldl](https://github.com/den1k/nldl): Natural Language for Clojure's Datalog flavor as present in Datomic, Datascript, Datahike etc.

### Other

* [clojurewerkz/ogre](https://github.com/clojurewerkz/ogre): Ogre is a Clojure Gremlin Language Variant of the Gremlin graph traversal language from Apache Tinkerpop, which is an open source, vendor-agnostic, graph computing framework.
* [stuartsierra/mapgraph](https://github.com/stuartsierra/mapgraph): Basic in-memory graph database of maps with links.
* [den1k/subgraph](https://github.com/den1k/subgraph): Reactive graph database for re-frame; a fork of stuartsierra/mapgraph.
* [keechma/keechma-entitydb](https://github.com/keechma/keechma-entitydb): EntityDB is a client side database and normalization engine.

Queries
-------
* [juxt/pull](https://github.com/juxt/pull): Like Datomic pull, but can be used on any map.
* [edn-query-language/eql](https://github.com/edn-query-language/eql): EQL is a declarative way to make hierarchical (and possibly nested) selections of information about data requirements.
  - [souenzzo/eql-style-guide](https://github.com/souenzzo/eql-style-guide): This guide covers both EQL as an abstract API and common library usage, like fulcro and pathom.
  - [wilkerlucio/pathom](https://github.com/wilkerlucio/pathom): Pathom is a Clojure(script) engine for processing EQL requests.
    * [wilkerlucio/pathom3](https://github.com/wilkerlucio/pathom3): Pathom3 is a redesign of Pathom.
    * [jlesquembre/pathom-pedestal](https://github.com/jlesquembre/pathom-pedestal): A library to integrate pathom and pedestal.
  - [graphqlize/honeyeql](https://github.com/graphqlize/honeyeql): HoneyEQL transforms EQL into efficient SQL.
  - [lilactown/pyramid](https://github.com/lilactown/pyramid): A library for storing and querying graph data in a Clojure map.
* [sixthnormal/pullql](https://github.com/sixthnormal/pullql): A GraphQL-like query language for DataScript, optimized for execution across many entities at once.
* [walkable-server/walkable](https://github.com/walkable-server/walkable): A Clojure(script) SQL library for building APIs: Datomic® (GraphQL-ish) pull syntax, data driven configuration, dynamic filtering with relations in mind.
* [walmartlabs/lacinia](https://github.com/walmartlabs/lacinia): This library is a full implementation of Facebook's GraphQL specification.
  - [vlaaad/plusinia](https://github.com/vlaaad/plusinia): Solution to N+1 problem in Lacinia.
* [graphqlize/graphqlize](https://github.com/graphqlize/graphqlize): A library for creating a GraphQL API for a Postgres or MySQL database.
* [timrichardt/hicgql](https://github.com/timrichardt/hicgql): GraphQL in Clojure data structures.
* [ivarref/clj-paginate](https://github.com/ivarref/clj-paginate): Pagination of vectors and maps with Clojure for GraphQL

Miscellaneous
------------
* [fulcrologic/fulcro](https://github.com/fulcrologic/fulcro): Fulcro is a full-stack web framework where a single underlying graph acts as the shared data model of both backend and frontend.
* [plumatic/plumbing](https://github.com/plumatic/plumbing): Plumbing and Graph: the Clojure utility belt. Graph is a simple and declarative way to specify a structured computation, which is easy to analyze, change, compose, and monitor.
* [simongray/datalinguist](https://github.com/simongray/datalinguist): Stanford CoreNLP in idiomatic Clojure. Support for dependency grammar graphs, pattern matching, and visualisation.
* [nwjsmith/generators.graph](https://github.com/nwjsmith/generators.graph): test.check generators for graph data.
* [jackrusher/mundaneum](https://github.com/jackrusher/mundaneum): A clojure wrapper around WikiData.
* [Swirrl/cubiql](https://github.com/Swirrl/cubiql): A proof of concept GraphQL service for querying Linked Data Cubes.

### Personal knowledge graphs
It is perhaps worth mentioning that several tools have been written in Clojure for making personal knowledge graphs through note-taking. The first one to appear was [Roam Research](https://roamresearch.com/) (proprietary). It has since inspired [Athens Research](https://github.com/athensresearch/athens) (open source, commercial) and [Logseq](https://github.com/logseq/logseq) (open source, community-driven). These tools are all based on libraries listed in the Datalog section.

Articles/video
--------------
* [Open Source Clojure-Datalog Databases](https://clojurelog.github.io/)
* [Domain modeling with Datalog](https://www.youtube.com/watch?v=oo-7mN9WXTw)
* [Introduction to Asami](https://github.com/threatgrid/asami/wiki/2.-Introduction)

Community
---------
RDF has a small, but steady Clojure following. People are using Neo4j with Clojure, but not talking much about it. Datomic-like Datalog databases have the most momentum.

* [Clojurians Slack](https://clojurians.slack.com/messages): Where Clojure's most active users seem to hang out.
  - [#rdf](https://clojurians.slack.com/archives/C09GHBXRC)
  - [#datalog](https://clojurians.slack.com/archives/CJ322KHNX)
  - [#datomic](https://clojurians.slack.com/archives/C03RZMDSH)
  - [#datascript](https://clojurians.slack.com/archives/C07V8N22C)
  - [#datahike](https://clojurians.slack.com/archives/CB7GJAN0L)
  - [#datalevin](https://clojurians.slack.com/archives/C01RD3AF336)
  - [#xtdb](https://clojurians.slack.com/archives/CG3AM2F7V)
  - [#neo4j](https://clojurians.slack.com/archives/C01BMKFSL14) - currently dead, but maybe you can make it come alive?
