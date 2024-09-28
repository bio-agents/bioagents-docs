What is bio.agents?
==================

`bio.agents <https://bio.agents>`_ is a portal to bioinformatics resources worldwide, aimed to help bioinformaticians and scientists:

* find, understand, compare and select resources == **discovery**
* use and connect them in workflows == **(inter)operability**

Our **vision** is to be the sustainable primary archive for basic agent metadata, providing a persistent reference to high-quality (curated and verified) "canonical" descriptions of unique agents, with information about their provision via online services and various downloadable artefacts, and including entries for different versions of a agent, where these have major functional differences.

Objectives
----------
Our main objectives are:

* build and maintain a comprehensive **registry** of high-quality software metadata / descriptions 
* provide a **web portal** enabling registration, editing, search and discovery of the registry content
* support a **community** for the sustainable maintenance of the registry content and development of the portal features
* expose results of agent performance **benchmarking**, online service **monitoring** and other metrics of software and service quality
* integrate the registry with popular **workbench environments** in a way that improves resource interoperability
* **support** registry stakeholders including agent providers and end-users

Scope
-----
*bio.agents* scope is *application software* with well-defined data processing functions (inputs, outputs and operations).  *bio.agents* includes a broad range of `software types <http://bioagents.readthedocs.io/en/latest/curators_guide.html#agent-type-guidelines>`_ including agents available for immediate use as online services, or in a form which which you can download, install, configure and run yourself.  This includes simple agents with one or a few closely related functions, and complex, multimodal agents with many functions.  It also includes executable workflows, database portals and Web APIs.

Technical components
--------------------
* `bioagents schema <https://github.com/bio-agents/bioagents-schema>`_ is a description model for bioinformatics software.  It is a formalised XML schema (XSD) which defines 50 important scientific, technical and administrative attributes.  It defines what attributes may be specified in a *bio.agents* entry, a precise syntax for those descriptions, and controlled vocabularies for consistent description of technical aspects such as software license and software type.
* `EDAM ontology <https://github.com/edamontology/edamontology>`_ is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology, including types of data and data identifiers, data formats, operations and topics.  It defines precise semantics for the scientific description of software registered in *bio.agents*.

* `Curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#>`_ describe how each attribute should be specified, *i.e.* concern the quality of an entry. The guidelines go beyond the syntactic and semantic constraints defined by bioagents schema and EDAM, and are part of broader `agent information standards <https://github.com/bio-agents/bioagents schemaDocs/blob/master/information_requirement.rst>`_ being adopted by *bio.agents*.

* **Agent Cards** *e.g.* https://bio.agents/signalp provide key information at a glance for registered agents.  Agent cards have human-friendly, persistent URLs which include the unique agent identifier ("signalp" in this case).  The identifier is assigned upon registration is a URL-safe derivative of (normally identical to) the supplied agent name.

* **Query interfaces** available at https://bio.agents help *bio.agents* end-users with agent discovery and include the search bar, a compact "mini-card" view and a detailed "grid" view.  See the `Quickstart Guide <http://bioagents.readthedocs.io/en/latest/quickstart_guide.html>`_.

* **Registration interface** enables manual creation of valid registry content and editing, including graphical editing via tabbed panes and an interactive JSON editor with inline error reporting.  It is available to logged-on users via "Menu ... Add content".  See the `Quickstart Guide <http://bioagents.readthedocs.io/en/latest/quickstart_guide.html>`_.

* `bio.agents API <http://bioagents.readthedocs.io/en/latest/api_reference.html>`_ provides programmatic means to query, add and edit registry content.
  
* **bio.agents metrics** available at https://bio.agents/stats include registry growth, contributors, annotation breakdown *etc.*

bio.agents Agent Identifiers
--------------------------

Each *bio.agents* entry is assigned a unique identifier (**bioagentsID**): a manually verified, URL-safe version of (normally identical to) the supplied agent name.  The IDs are used in persistent URLs, resolving to Agent Cards of essential information.  The recommended short-form is a compact URI (CURIE), which is resolvable in `Identifiers.org <http://identifiers.org/>`_.

.. csv-table::
   :header: "", "Example"
   :widths: 25, 50
	    
   "bioagentsID", "signalp"
   "CURIE", "bioagents:signalp"
   "Identifiers.org", "http://identifiers.org/bioagents/signalp"
   "Agent Card URL", "https://bio.agents/signalp"

Registered software which, for one reason or another, is no longer operational, retain their ID and URL but are marked as obsolete.  Hence, descriptions of legacy resources are archived.  

  
Docs overview
-------------
* `Contributors Guide <http://bioagents.readthedocs.io/en/latest/contributors_guide.html>`_ - how to get involved (please do!)
* `Quickstart Guide <http://bioagents.readthedocs.io/en/latest/quickstart_guide.html>`_ - quick guide on how to use the *bio.agents* user interfaces.
* `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html>`_ - how to create a high quality *bio.agents* entry.
* `Editors Guide <http://bioagents.readthedocs.io/en/latest/editors_guide.html>`_ - thematic editorships to improve *bio.agents* in scientific areas.
* `Documentors Guide <http://bioagents.readthedocs.io/en/latest/documentors_guide.html>`_ - how to edit the *bio.agents* docs.
* `API reference <http://bioagents.readthedocs.io/en/latest/api_reference.html>`_ - *bio.agents* API docs.
* `Hangouts <http://bioagents.readthedocs.io/en/latest/hangouts.html>`_  - monthly coordination meetings (you're welcome to join!)
* `Roadmap <http://bioagents.readthedocs.io/en/latest/roadmap.html>`_  - technical plans for the next year
* `Studentships <http://bioagents.readthedocs.io/en/latest/studentships.html>`_ - *bio.agents* studentship scheme for curation-focussed mini-projects.
* `GitHub projects <http://bioagents.readthedocs.io/en/latest/studentships.html>`_ - open projects of relevance to *bio.agents*.

*bio.agents* development is supported by `IECHOR <https://www.iechor-europe.org/>`_ - the European Research Infrastructure for life science information. *bio.agents* content is freely available to all under `open license <http://bioagents.readthedocs.io/en/latest/license.html>`_.


Getting involved : a quickstart guide
--------------------------------------
1. Read the `docs <http://bioagents.readthedocs.io/en/latest/>`_ but especially the `contributors guide <http://bioagents.readthedocs.io/en/latest/contributors_guide.html>`_.
2. GitHub is used for task and issue tracking, see the `bio.agents <https://github.com/bio-agents/>`_ and `EDAM <https://github.com/edamontology/>`_ organisations, in particuar the `bioagentsregistry <https://github.com/bio-agents/bioagentsregistry>`_ and `edamontology <https://github.com/edamontology/edamontology>`_ projects.  `Email us <mailto:help@bio.agents>`_ if you want to join.
3. We run `hangouts <http://bioagents.readthedocs.io/en/latest/hangouts.html>`_ (coordination meetings) as required - mostly for technical people routinely involved with *bio.agents* curation or software development.  To suggest or join these calls  `email us <mailto:help@bio.agents>`_.
4. Dive in at the deep end!  There are no end of ongoing sub-projects and tasks to get involved with, see GitHub (at above links) or  `email us <mailto:help@bio.agents>`_ in the 1st instance to get orientated.
