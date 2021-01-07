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
* [ekoontz/dag-unify](https://github.com/ekoontz/dag-unify): A Clojure library for combining directed acyclic graphs (DAGs) via unification.

Visualisation
-------------
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
* [Swirrl/csv2rdf](https://github.com/Swirrl/csv2rdf): Clojure library and application implementing the [W3C CSV on the Web tabular metadata specifications](https://w3c.github.io/csvw/) for converting CSV to RDF.
* [ont-app/vocabulary](https://github.com/ont-app/vocabulary): Utilities to map between clojure namespaced keywords and RDF-style URIs.
* [phillord/tawny-owl](https://github.com/phillord/tawny-owl): Tawny-OWL allows construction of OWL ontologies, in a evaluative, functional and fully programmatic environment.
  - [phillord/owl-primer](https://github.com/phillord/owl-primer): The Ontology from the owl-primer written using Tawny-OWL.
* [sam_russell/porta-owl-sqwrl](https://gitlab.com/sam_russell/porta-owl-sqwrl): (GITLAB) A Clojure domain-specific language for Web Ontology Language (OWL) and Semantic (Query) Web Rule Language (SQWRL).

### Datalog
Clojure's Datomic-like databases also model data as triplets... or technically as quintuplets AKA datoms.

* [Datomic.com](https://www.datomic.com/): _(PROPRIETARY)_ A transactional database with a flexible data model, elastic scaling, and rich queries.
  - [vvvvalvalval/datofu](https://github.com/vvvvalvalval/datofu): This library provides common utilities for working with Datomic, mostly in the form of database functions.
  - [vvvvalvalval/datalog-rules](https://github.com/vvvvalvalval/datalog-rules): Utilities for managing Datalog rulesets from Clojure.
  - [Provisdom/spectomic](https://github.com/Provisdom/spectomic): Generate Datomic or Datascript schema from your Clojure(script) specs.
  - [ont-app/datomic-client](https://github.com/ont-app/datomic-client): Ports the Datomic Client to the IGraph protocols.
* [tonsky/datascript](https://github.com/tonsky/datascript): An immutable in-memory database and Datalog query engine in Clojure and ClojureScript.
  - [mpdairy/posh](https://github.com/mpdairy/posh): Posh is a ClojureScript / React library that lets you use a single DataScript database to store your app state.
  - [denistakeda/re-posh](https://github.com/denistakeda/re-posh): Re-posh allows Posh and re-frame to work together by adding support for re-frame specific subscriptions, events, effects, and co-effects to Posh.
  - [metasoarous/datsync](https://github.com/metasoarous/datsync): This library offers tools for building DataScript databases as materialized views (very much in the re-frame/samsa sense) of some master/central Datomic database.
  - [ont-app/datascript-graph](https://github.com/ont-app/datascript-graph): An implementation of the IGraph protocol extended to datascript.
* [replikativ/datahike](https://github.com/replikativ/datahike): Datahike is a durable Datalog database powered by an efficient Datalog query engine.
  - [replikativ/datahike-frontend](https://github.com/replikativ/datahike-frontend): A front-end to Datahike written in Fulcro.
* [juji-io/datalevin](https://github.com/juji-io/datalevin): Datalevin is a simple durable Datalog database.
* [threatgrid/asami](https://github.com/threatgrid/asami): An in-memory graph database, for Clojure and ClojureScript.
  - [threatgrid/asami-loom](https://github.com/threatgrid/asami-loom): This library extends Asami in-memory graphs to Loom.
* [juxt/crux](https://github.com/juxt/crux): Crux is a general purpose database with graph-oriented bitemporal indexes.
* [Workiva/eva](https://github.com/Workiva/eva): Eva is a distributed database-system implementing an entity-attribute-value data-model that is time-aware, accumulative, and atomically consistent.
* [threatgrid/naga](https://github.com/threatgrid/naga): Datalog based rules engine.
* [den1k/nldl](https://github.com/den1k/nldl): Natural Language for Clojure's Datalog flavor as present in Datomic, Datascript, Datahike etc.

### Other

* [clojurewerkz/ogre](https://github.com/clojurewerkz/ogre): Ogre is a Clojure Gremlin Language Variant of the Gremlin graph traversal language from Apache Tinkerpop, which is an open source, vendor-agnostic, graph computing framework.
* [stuartsierra/mapgraph](https://github.com/stuartsierra/mapgraph): Basic in-memory graph database of maps with links.
* [den1k/subgraph](https://github.com/den1k/subgraph): Reactive graph database for re-frame; a fork of stuartsierra/mapgraph.
* [keechma/keechma-entitydb](https://github.com/keechma/keechma-entitydb): EntityDB is a client side database and normalization engine.

Queries
-------
* [edn-query-language/eql](https://github.com/edn-query-language/eql): EQL is a declarative way to make hierarchical (and possibly nested) selections of information about data requirements.
  - [wilkerlucio/pathom](https://github.com/wilkerlucio/pathom): Pathom is a Clojure(script) engine for processing EQL requests.
  - [graphqlize/honeyeql](https://github.com/graphqlize/honeyeql): HoneyEQL transforms EQL into efficient SQL.
* [sixthnormal/pullql](https://github.com/sixthnormal/pullql): A GraphQL-like query language for DataScript, optimized for execution across many entities at once.
* [walmartlabs/lacinia](https://github.com/walmartlabs/lacinia): This library is a full implementation of Facebook's GraphQL specification.

Miscellaneous
------------
* [fulcrologic/fulcro](https://github.com/fulcrologic/fulcro): Fulcro is a full-stack web framework where a single underlying graph acts as the shared data model of both backend and frontend.
* [plumatic/plumbing](https://github.com/plumatic/plumbing): Plumbing and Graph: the Clojure utility belt. Graph is a simple and declarative way to specify a structured computation, which is easy to analyze, change, compose, and monitor.
* [simongray/datalinguist](https://github.com/simongray/datalinguist): Stanford CoreNLP in idiomatic Clojure. Support for dependency grammar graphs, pattern matching, and visualisation.
* [nwjsmith/generators.graph](https://github.com/nwjsmith/generators.graph): test.check generators for graph data.

Community
---------
RDF has a small, but steady Clojure following. People are using Neo4j with Clojure, but not talking much about it. Datomic-like Datalog databases have the most momentum.

* [Clojurians Slack](https://clojurians.slack.com/messages): Where Clojure's most active users seem to hang out.
  - [#neo4j](https://clojurians.slack.com/archives/C01BMKFSL14)
  - [#rdf](https://clojurians.slack.com/archives/C09GHBXRC)
  - [#datalog](https://clojurians.slack.com/archives/CJ322KHNX)
  - [#datomic](https://clojurians.slack.com/archives/C03RZMDSH)
  - [#datascript](https://clojurians.slack.com/archives/C07V8N22C)
  - [#datahike](https://clojurians.slack.com/archives/CB7GJAN0L)
  - [#crux](https://clojurians.slack.com/archives/CG3AM2F7V)
