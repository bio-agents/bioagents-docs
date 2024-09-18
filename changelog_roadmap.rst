Roadmap
=======
A summary of planned technical development of bio.agents software.  Developments are informed by the IECHOR EXCELERATE application (granted in April 2015).  The roadmap is updated in light of community input (see `Contributors Guide <http://bioagents.readthedocs.org/en/latest/hangouts.html>`_) and on-going developments.  As a rule we aim for quarterly registry feature releases with supporting EDAM releases.


  
2017 Q3
-------

- curation

  - *content quality is now the priority aiming for 10,000 entries by Dec 2016*
  - clean-up of `agentd names / IDs <https://bioagents.sifterapp.com/issues/401>`_
  - consolidation of `duplicates <https://bioagents.sifterapp.com/issues/297>`_ (Q3-Q4)
  - systematic identification of rightful entry owners:  email requesting adoption of entries, request new agents (Q2-)
  - systematic `annotation of agent publication IDs <https://bioagents.sifterapp.com/issues/224>`_
  - systematic improvement of entries following QC checks (Q2-) 
  - curation of agents from msutils.org to “gold-standard” via `studentship <https://bioagents.sifterapp.com/issues/177>`_ (Q2-Q3)

- features / technical

  - extra enhancements to content reporting (total #annotations, #annotations vs. time, annotations by type: table, chart)
  - indexing of whole site following clean-up of duplicates and agent IDs
  - expose #citations, altmetric attention score 
  - support for bioagentsSchema 2.0.0 XML format I/O
  - (mock up) new Curator Agenting
  - (prototype) Metrics Card with infographic showing compliance to information standard
  - (scoping) implementation of integration with BioShadock, BioContainers etc. (containers), IFB cloud (VMs, workflows)  


- docs

  - finalise `entry quality metrics <https://bioagents.sifterapp.com/issues/243>`_ : see the `emerging standard <https://github.com/bio-agents/bioagentsSchemaDocs/blob/master/information_requirement.rst>`_ and join the `discussion on GitHub <https://github.com/bio-agents/bioagentsSchema/issues/77>`_
  - finalise the `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html”>`_

    
- IECHOR EXCELERATE WP1 Deliverables & milestones

  - D1.2 - `registry release <https://bioagents.sifterapp.com/issues/257>`_
  - D1.5 - `metrics in registry <https://bioagents.sifterapp.com/issues/256>`_
  - D1.6 - `workbench integration enabler <https://bioagents.sifterapp.com/issues/258>`_
  - M1.1.2 - `EDAM release + agenting <https://bioagents.sifterapp.com/issues/252>`_
  - M1.3 - `literature integration <https://bioagents.sifterapp.com/issues/253>`_
  - M1.4 - `close-to-source annotation <https://bioagents.sifterapp.com/issues/254>`_
  - M1.7.1 - `novel user interfaces <https://bioagents.sifterapp.com/issues/255>`_

- *revisions in light of EXCELERATE midterm review tbd* -
    
2017 Q4
-------
- curation

  - planning of comprehensive coverage & systematic improvment in scientific areas via  `"thematic editors" <https://bioagents.sifterapp.com/issues/374>`_

- features / technical

  - improved search and filtering
  - drop mandatory requirement for email or URL in credits (non-breaking change in bioagentsSchema 2.1.0 and UI)
  - sorting on #citations, altmetric score, publication date *etc.*
  - graph of #citations, altmetric score *etc.* by time
  - expose publication metadata, *e.g.* copy-pastable citation information
  - extra enhancements to content reporting (*e.g.* contributors by top-level domain, contributors by geographic location, contributing institutes *etc.*)
  - begin implementation of integration with BioShadock, BioContainers etc. (containers), IFB cloud (VMs, workflows)
  - begin implementation of new bio.agents UI including Agent Annotator and icon-based navigation
  - begin implementation of Curator Agenting


Beyond 2017
-----------

- features / technical

  - "agents similar to these" feature (using EDAM annotations)
  - "drive-by curation" (suggestions from non-account holders)
  - add BioSchema Agent Specification mark-up, assess impact on presentation of search results
  - provide metadata as service (tbd)  

- evaluate user impact

  - assess agent discoverability (agent cards, agent homepage URLs) via Google



  
- M1.1.3 EDAM release with coverage of different resource categories and RIs. Implementation of agenting for sustainable community development
- M1.5 Good Practice Guidelines
- M1.6 Implementation of resource metadata catalogue & evaluation of impact of Resource Synergy Meeting series
- M1.7.2 Implementation of novel highly usable interfaces from analysis of user experience and usability requirements
- D1.3 Registry release with comprehensive coverage of IECHOR Node resources, including resource data format curation and analysis (Task 1)
- D1.7 Description of the registry user helpdesk & impact on user support via community forums (Task 4)
- D1.8 Matchmaking service: implementation & evaluation of impact
- M1.1.4 EDAM release with coverage of different resource categories and RIs. Implementation of agenting for sustainable community development
- D1.4 Registry release with comprehensive coverage of IECHOR Node resources, including resource data format curation and analysis (Task 1)
- integration with `DebianMed <https://bioagents.sifterapp.com/issues/32>`_



NOTE
----

- Things mentioned previously that will **not** be done

  - "sandbox" area for intermediate registrations.  The information requirement is now lower for `beta entries <https://github.com/bio-agents/bioagentsSchema#information-requirements>`_ , "sandbox" (staging area) is not needed
  - "moderation interface" for mass content import.  Instead there will be enhanced QA/QC with features for improving entries (see below)
  - improved admin interface for content management.  Instead an admin will be able to edit any entry via the UI, also programmatically via Python notebooks (see below)
  

      
Changelog
=========

A summary of technical developments of bio.agents software to date.

2017 Q2
-------

- curation

  - import of agents from `NAR Web servers <https://bioagents.sifterapp.com/issues/245>`_
  - import of agents from `Bioinformatics Links Directory - software <https://bioagents.sifterapp.com/issues/242>`_

- features / technical
  
  - SEO in preparation for indexing the whole site
  - (scoping) `Icon / topic-based view <https://bioagents.sifterapp.com/issues/172>`_ for browsing bio.agents
  - (prototype) `Agent Annotator <https://bioagents.sifterapp.com/issues/211>`_ UI
  - (mock-up) of new bio.agents UI (splash page, sub-pages, summary view, grid view)
  - "disown" entry button (My Profile)
  - improved search and filtering
  - proof-of-principle of `interactive diagrams <https://bioagents.sifterapp.com/issues/65>`_ of published workflows / agent-specific diagrams (https://bio.agents/worklows)

- docs

  - update `API documentation <http://bioagents.readthedocs.io/en/latest/api_reference_dev.html>`_ including attributes `JSON model <http://bioagents.readthedocs.io/en/latest/api_attribute_model_dev.html>`_
     
     
April 2017
----------


March 2017
----------
- subdomains

  - pilot for de.NBI, others
  - subdomain management in My Profile

February 2017
-------------
- enhanced content ownership / sharing features

  - "request edit rights" button (Agent Card)
  - "request ownership" button (Agent Card, My Profile)

- improved search

  - support "Collection" and "Credit" in search bar, with drop-down of suggestions
  - tweak search behaviour to address most critical issues from https://bioagents.sifterapp.com/issues/274


    
January 2017
------------
- Admin agenting

  - admin editing via UI
  - admin editing programmatically via Python notebooks
  
- improved QA/QC process (content monitoring & reporting)

  - comprehensive basic checks (see `technical proposal <https://docs.google.com/document/d/1ATj2zJOlbR3Edk6QyGvPX5HStZBknqfx1Fwqk4k0kqE/edit#heading=h.fffoc8urhpt8>`_)
  - labelling of entries with "has issues" **will not be done**  
  - reporting to admin page.  Reporting to Agent Cards & My Profile **will not be done**

- mass content imports  
  
  - `Agents used by EBI Training team <https://bioagents.sifterapp.com/issues/70>`_
  - `Agents used by IECHOR trainers <https://bioagents.sifterapp.com/issues/60>`_
  - `BioConductor <https://bioagents.sifterapp.com/issues/31>`_
  - `msutils.org <https://bioagents.sifterapp.com/issues/28>`_
  - `SEQwiki <https://bioagents.sifterapp.com/issues/27>`_
  - `Ontologies from OBO Foundry  <https://bioagents.sifterapp.com/issues/300>`_
  - `Ontology metadata from OLS <https://bioagents.sifterapp.com/issues/298>`_



December 2016
-------------
- stable data model, `bioagentSchema 2.0.0  <https://github.com/bio-agents/bioagentsSchema/tree/master/versions>`_ released

  - defines the stable bio.agents API
  - many major changes (new credit mechanism, cleaner aggregation of links, links (including for docs and downloads) can be typed etc.
  - breaking changes reserved to once/year from now on
  - incorporates very many community requests (tracked on https://github.com/bio-agents/bioagentsSchema/issues)
  - new `schema docs <https://bioagentsschema.readthedocs.io/en/latest/>`_

- support for candidate stable schema (Stage 1/3) in backend & user interfaces, revised documentation

- content migration to stable schema

  - created system for semi-automated migration of content (future proofing)
  - migrated existing content (Stage 1/3), see `Data model docs <https://docs.google.com/document/d/1tqw7FELV4F_qzrTA9KpVYoORAeFPyY1ZOjaGTPN2H1E/edit>`_

- labelling of all entries as "beta"

  - beta entries will require QC / user verification before being indexed

- Google indexing of bio.agents

  - new indexing system (keywords and metadata representation), no longer uses prerender, Google can now index single-page applications (Javascript)
  - main site is indexed, individual Agent Cards will be indexed as we migrate from "beta" entries

- new look Agent Cards

- bio.agents updated for EDAM_16

- support for EDAM synonyms for registration via API
  
November 2016
-------------

- revised https://bio.agents/stats pages with new graphs, cleaner look and feel etc.
- revised search mechanism, now performs exact and fuzzy searches
- revised Registration Interface, now provides inline error reporting
- feature to send verification (for account creation) and password reset emails
- features to share resources moved to "my profile" page
- scheduling system for housekeeping, e.g. gathering stats for https://bio.agents/stats
- misc. bug fixes  

October 2016
------------
- moved dev.bio.agents into production (consolidation of dev.bio.agents & bio.agents content) with QC check for redundant agent names 

- content ownership / sharing of edit rights (Google docs style)

  - ownership is not based on affiliation anymore, 1 owner / agent, edit rights can be shared with selected account holder, or with all account holders

- stable agent ID / URL scheme including agent version number

  - moved away from affiliation-name-version triplet for identifying entries, agents now identified by agentID, specific versions of a agent identified by versionID.  IDs have syntax constraints (defined in https://github.com/bio-agents/bioagentsSchema/).
  - IDs and therefore Agent Card URLs will be user-verifiable (implementation tbd)

- improved bio.agents auto-mailer (using admin email address)

- added historical stats to bio.agents/stats

  
July 2016
---------
- rewrite bio.agents software to pay off technical debt (completed)

June 2016
---------
- ~750 automated unit tests
- new and improved grid view
- "my profile" page, with account information and list of agents registered by this account
- Curation admin interface (content edition) (beta)
- General admin interface (account management, password change, reset etc) (beta)

May 2016
--------
- robust validation of incoming agent descriptions
- new URL / persistent ID scheme
- unit tests for EDAM topics, operations, data types and formats


April 2016
----------
- bio.agents/stats page
- improved load time
- added Elasticsearch support for improved search
- user authentication support for password change, reset, etc
- new improved and simplified search and filtering interface (neXtProt style)

March 2016
----------
- bio.agents documentation framework: https://bioagents.readthedocs.org
- rewrite bio.agents software to pay off technical debt (on-going)

December 2015
-------------
- Created URL links to various registry related resources, such as bio.agents/events
- Displaying date added as 'time ago'
- Improvements to the pagination
- Added a nightly validator that ensures that the existing contents of the registry validate against the XSD schema
- EDAM release
- Continuous debugging and improvements

November 2015
-------------
- Created a mechanism for gathering stats of the current content of the registry
- API now returns date of last update
- Sorting entries by last added
- Improvements to the account creation
- Schema release
- Continuous debugging and improvements

October 2015
------------
- Rework of all interfaces to make website mobile friendly
- Improved error handling, messages and display when registering a resource
- Made JSON interactively editable in the Â¡Â®Resource registrationÂ¡Â¯ interface
- Continuous debugging and improvements

September 2015
--------------
- New domain bio.agents
- New advanced filtering widget and mechanism
- Improvements to the EDAM widget
- Agenttips redone
- Updated the contact tab in Â¡Â®Resource registrationÂ¡Â¯ to make it obvious that either email or URL is required instead of both
- Continuous debugging and improvements

August 2015
-----------
- Major release with focus on improved interface usability:
  - Removed splashscreen
  - Refactored menus
  - New browsing interface: added new Â¡Â®pillÂ¡Â¯ view, new sorting capabilities, storing search state in the URL etc.
  - New registration interface: new ontology browsing widget, restructured to improve look and feel
  - New editing interface (for existing resources)
  - Added Â¡Â®compact viewÂ¡Â¯ to query interface
  - Improved search bar with search suggestions
- Finalizing search API intended to prepare for growth in content and usage of the registry (scalability)
- New transferable search URL - same syntax for filtering both via GUI and API
- Continuous debugging and improvements

July 2015
--------- 
- Work on a search API intended to prepare for growth in content and usage of the registry (scalability)
- Implemented Resource Pages (mature)
  - New look: compactified, visualisation of functions and in/outputs
- Work on major enhancements to interface usability
- Continuous debugging and improvements

June 2015
---------
- bioagentsXSD-1.2 released
  - https://github.com/jongithub/bioagentsxsd/blob/master/CHANGELOG.md
- Registry software updated to accommodate the new release (ongoing)
- Continuous debugging

May 2015
--------
- Created new demo server
- Created replacement page for use upon releases
- Set up Google Indexing
- Enabled Google Analytics
- Implemented Resource Pages (beta)
- Made publication attribute mandatory
- Created bioagentsXSD project in Github
- bioagentsXSD-1.1 released
  - https://github.com/jongithub/bioagentsxsd/blob/master/CHANGELOG.md 
  - Updated schema docs for "Name" standards
  - Updated schema docs to include simple table of attributes (optional, recommended, mandatory) PLUS reference Google Doc with this info
- Continuous debugging

April 2015
----------
- Added ability to adjust column width 
- Added ability to sort columns
- Outlined technical implementation of Resource Pages
- Enforced "name" standards in registration interface
- Prepare for Google Indexing
- Added whole VM deployment and provisioning setup
- Various schema updates, e.g.
  - Improved dataType, dataFormat element docs
  - Extended URL with support for FTP 
  - Enforced Â¡Â®description' length limit
  - Enforced other 'description' fieldsÂ¡Â¯ length limits
  - Made publication ID mandatory
  - Updated sample JSON with "null" value of "uri"
- Continuous debugging

March 2015
----------
- Batch registration to support XML format, & support multi-resource JSON / XML upload
- Fixed the interface not to direct the user to the splash screen all the time
- Various schema updates, e.g.
  - Harmonize "Maturity" in software description schema
  - Updated comment in schema docs for "contact"
  - Removed URI from softwareType and resourceType
  - Updated schema for missing AppDB languages
  - Updated schema for missing AppDB licenses
- Continuous debugging

February 2015
-------------
- Released EDAM 1.9 with corresponding registry updates
- Splash page updated to accept full term before redirecting
- Various schema updates, e.g.
  - Added "virtual appliance" to enum for interfaceType
  - Removed URLs from simple enums in schema (old SWO terms)
  - Changed "Accessibility" element to support "private" agents 
  - Added "Dataset" to enum for resourceType
- Continuous debugging
