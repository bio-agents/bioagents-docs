Status reports
==============

2017 January
------------

See the `changelog and roadmap <http://bioagentsschema.readthedocs.io/en/latest/>`_

  - IECHOR Hackathon @ EuBIC Winter School, Jan 10 2017 (https://tinyurl.com/registryhackathon11)

  - IECHOR bio.agents Curation Workshop: Genomics Agents and Databases in Agricultural Science Feb 2-3 2017 (https://tinyurl.com/registryhackathon12)

  - First draft of "registry pillar" of `IECHOR Agents Platform roadmap <https://docs.google.com/document/d/1rWzWdxMJvSkDRWEfdyMSu8EMO0LfV_UXwsG86JZmIZ0/edit#heading=h.j77fai7pe4sc>`_  : *open for comments*


**ACTIONS**

See `roadmap <http://bioagents.readthedocs.io/en/latest/changelog_roadmap.html>`_ :

  - tweak search behaviour to address most critical issues from https://bioagents.sifterapp.com/issues/274
  - drop mandatory requirement for email or URL in credits (non-breaking change for 2.1.0)
  - clarify what is meant by "beta", maybe change label to "This entry has not been manually verified"
  - set up access to repo for Kenzo et al.
    

2016 December
-------------
Actions (November)
^^^^^^^^^^^^^^^^^^
  - Technical developments

     - stable schema `bioagentsSchema 2.0.0 <https://github.com/bio-agents/bioagentsSchema/tree/master/versions/bioagents-2.0.0>`_ released.  It will define the scope and potential functionality of bio.agents for years to come.   Future versions will follow the MAJOR.MINOR.PATCH pattern (http://semver.org), with major changes that could break bio.agents API dependencies restricted to once/year.  
     - EDAM_1.16 released and available on `BioPortal <http://bioportal.bioontology.org/ontologies/EDAM?p=classes>`_ and `OLS <https://www.ebi.ac.uk/ols/ontologies/edam>`_.
       
  - Documentation
    
     - new schema docs on http://bioagentsschema.readthedocs.io/en/latest/
     - information requirement for "beta" and "standard" bio.agents entries `defined here <https://github.com/bio-agents/bioagentsSchema#information-requirements>`_.
    
     
Plans (December)
^^^^^^^^^^^^^^^^

  - Technical work towards the Dec release, see  `roadmap <http://bioagents.readthedocs.io/en/latest/changelog_roadmap.html>`_ of registry software developments
  - Various content additions listed on `sifterapp <https://bioagents.sifterapp.com/projects/39503/issues?srt=priority>`_  
  - WP 1 / IECHOR-DK partners telcon 10AM UK, Fri Dec 2

2016 October
------------

Actions (October)
^^^^^^^^^^^^^^^^^
  - Technical developments

     - `dev.bio.agents <https://dev.bio.agents>`_ has been moved into production on https://bio.agents.  Including new content ownership model whereby edit rights on entries can be shared amongst bio.agents users.
     - candidate stable schema `bioagentsSchema 2.0-beta02 <https://github.com/bio-agents/bioagentsSchema/tree/master/bioagents-2.0-beta-02>`_ released.
     - prototype EDAM extension for bioimaging analysis concepts released : `EDAM-Bioimaging_alpha01 <http://bioportal.bioontology.org/ontologies/EDAM-BIOIMAGING?p=classes>`_. 

  - Outreach actions

     - Bioschema specification for schema.org mark-up for agents on the Semantic Web, worked on during `NETTAB hackathon <http://tinyurl.com/registryhackathon10>`_.  Such mark-up will be added to bio.agents Agent Cards in due course.
     - revision / extension of `bio.agents documentation <bioagents.readthedocs.io/en/latest/>`_
     - new `EDAM documentation <http://edamontologydocs.readthedocs.io/en/latest/>`_ and revamp of https://edamontology.org.
     - bio.agents `studenstship scheme <http://bioagents.readthedocs.io/en/latest/studentships.html>`_ now available

  - Content

     - consolidation of content from dev.bio.agents and bio.agents : 2885 entries, 376 contributors (registered users)
     - top-down plan for content expansion now `available <https://docs.google.com/document/d/1AM0iLimpT4ClybEKYYdWu52RzJ9GKqUpW2DZflS6_4c/edit>`_ for comment.  See `sifterapp issue <https://bioagents.sifterapp.com/issues/241>`_. 


Plans (November)
^^^^^^^^^^^^^^^^
  - Technical work towards the Dec release, see  `roadmap <http://bioagents.readthedocs.io/en/latest/changelog_roadmap.html>`_ of registry software developments 
  - import of SEQwiki (see `sifterapp issue <https://bioagents.sifterapp.com/issues/27>`_.)
  - EDAM 1.16 including requests via GitHub and addition of data format concepts


2016 September
--------------

Actions (September)
^^^^^^^^^^^^^^^^^^^
 
  - Major recent work highlights
     - finished rewrite of registry software (see https://dev.bio.agents) 
     - major revision of underlying data model (bioagentsXSD) producing candidate stable schema (https://github.com/bio-agents/bioagentsxsd/)
     - Deliverable D1.1 submitted on time
     - Presentation of work at ISMB, ECCB and DKBC
     - improved & extended `bio.agents docs <http://bioagents.readthedocs.io/en/latest/>`_
     - detailed `roadmap <http://bioagents.readthedocs.io/en/latest/changelog_roadmap.html>`_ for registry software developments 
     - paper submitted   "ReGaTE, Registration of Galaxy Agents in iEchor" Olivia Doppelt-Azeroual, Ph.D.; Fabien Mareuil, Ph.D.; Eric Deveaud; Matus Kalas, Ph.D.; Nicola Soranzo; Marius van den Beek, Ph.D.; Björn Grüning; Jon Ison; Hervé Ménager

Plans (October)
^^^^^^^^^^^^^^^

     - moving dev.bio.agents into production, see  `roadmap <http://bioagents.readthedocs.io/en/latest/changelog_roadmap.html>`_ for registry software developments 
     - `top-down plan for content expansion <https://bioagents.sifterapp.com/issues/241>`_


2016 June
---------- 

Actions (June)
^^^^^^^^^^^^^^^
  - Content
     - Mapping of OLS tags : EDAM (proposal), hopefully OLS will adopt EDAM.  See https://bioagents.sifterapp.com/issues/186.

  - Outreach actions

    - ASMS/IMSC conference
      - Magnus Palmblad (LUMC, NL) et al - member of registry-core - submitted a poster on workflow composition using EDAM / bio.agents annotations.

    - ISMB
      - Prepare 5 posters (IECHOR & IECHOR-DK, IECHOR EXCELERATE WP1, bio.agents, EDAM, bioagentsXSD, computerome)
      - Booth preparations (freebies, dressing etc.) & logistics

    - Meeting with representatives of `The Open Microscopy Environment <https://www.openmicroscopy.org/>`_ and `Euro-BioImaging <www.eurobioimaging.eu/>`_  (including Gloabl-BioImaging) scope technical for collaboration with bio.agents.  See https://bioagents.sifterapp.com/issues/166.


  - Technical specification documents

    - "Agent types and relations" (1st draft) to inform bioagentsXSD 2.0 development and support re-use of agent descriptions, and reduce duplications and inconsistencies in bio.agents.

  - Technical developments

    -          ~750 automated unit tests
    -          new and improved grid view
    -          ‘my profile’ page, with account information and list of agents registered by this account
    -          admin / curation interface (work ongoing)

    - Continue bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_, with a focus on user interfaces and unit tests
    - Curation admin interface (content edition) (beta)
    - General admin interface (account management, password change, reset etc)

- Tasks **not** completed

  - Prepare new slide deck for Tech Track including software demo

Plans (July)
^^^^^^^^^^^^^^^^

  - Technical developments
     - migrating and consolidating the content from the production database to the new system
     - testing improvements to the search (so that it returns more relevant results)
     - quality of life improvements to the registration interface (error handling)
     - work towards release new system for testing by registry-core 

  - Outreach actions
     - ISMB

  - Technical specification documents
     - Settle these in prep for EXCELERATE WP1 D1.1
       - API specs
       - Agent types and relations
       - Content ownership model
       - Improved agent annotator mock-up 



Notes
^^^^^^^^^^^

  The “Agents, Workflows and Workbenches” hackathon (Institut Pasteur, May 18-20) was co-organized by the French and Danish IECHOR nodes.  The event brought together over 40 representatives from 21 academic institutions and companies, with projects including Galaxy, bio.agents, Common Workflow Language, bioagentsXSD, EDAM, Debian Med, BioShadock and more.  The delegates enjoyed a series of talks, lively discussions and breakout hacking sessions including bio.agents entry relationships, Galaxy to bio.agents publishing, CWL specification, workflow specification interoperability, and training workflows.  In addition to concrete outcomes including various technical documents, new CWL bindings and enabling support for EDAM annotations in Galaxy, the hackathon provided a boost to various ongoing collaborations between the projects and institutes.  We look forward to a re-run soon!




2016 May
---------- 

Actions (May)
^^^^^^^^^^^^^^^
- Outreach actions (see https://bio.agents/events)

  - At ISMB, IECHOR-DK will have a booth a give a technology track presentation
  - The “Agents, Workflows and Workbenches” hackathon (Institut Pasteur, May 18-20) was attended by over 40 people.  See `tinyurl.com/registryhackathon8 <tinyurl.com/registryhackathon8>`_ and the summary (below).

- Development of the improved agent annotator is being led by Hans-Ioan Ienasescu, based on the `mockup <https://docs.google.com/document/d/1IJLMu_5WSJmFa6ePmL034ju7mPG8GBYMYxLixmiRDMI/edit#>`_

- Content

    - EDAM 1.15 is out
        It includes new community-requested concepts and terms, including for metagenomics and biodiversity, structural improvements and fixes (synonyms clean-ups etc.), format updates, and implification of some concepts.  See the `Change log <https://github.com/edamontology/edamontology/blob/master/changelog.md>`_. Browse EDAM on `BioPortal <http://bioportal.bioontology.org/ontologies/EDAM?p=classes>`_ and in the new `OLS <http://www.ebi.ac.uk/ols/ontologies/edam>`_.

- bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_ . Features done but not yet in production:

  - **back-end** development

    - robust validation of incoming agent descriptions
    - new URL / persistent ID scheme
    - unit tests for EDAM topics, operations, data types and formats

  - **front-end** development

    - ongoing work on the admin / curator interface
    - ongoing work on the improved grid view


Plans (June)
^^^^^^^^^^^^^^^^

  - Outreach actions

    - ISMB
      - Prepare 5 posters (computerome, IECHOR-DK, bio.agents, EDAM, bioagentsXSD)
      - Prepare new slide deck for Tech Track
      - Booth preparations (freebies, dressing etc.)
      - Plan logistics

    - Meeting with representatives of `The Open Microscopy Environment <https://www.openmicroscopy.org/>`_ and `Euro-BioImaging <www.eurobioimaging.eu/>`_ to scope out technical collaboration with bio.agents.


  - Technical specification documents

    - "Agent types and relations" (1st draft) to inform bioagentsXSD 2.0 development and support re-use of agent descriptions, and reduce duplications and inconsistencies in bio.agents.

  - Technical developments

    - Continue bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_, with a focus on user interfaces and unit tests
    - Curation admin interface (content edition) (beta)
    - General admin interface (account management, password change, reset etc)

- Tasks **not** completed in May

  - General admin interface (account management, password change, reset etc) - postponed for now



2016 April
---------- 

Actions (April)
^^^^^^^^^^^^^^^
- Outreach actions (see https://bio.agents/events)

  - Metagenomics Thematic Hackathon (7-8)
  - Slovenian Agents Curation Hackathon (8)
  - Preparations for `ECCB 2016 <https://bioagents.sifterapp.com/issues/154>`_:
 
    - IECHOR-DK booth
    - IECHOR Application Track submissions
 
      - bio.agents - status and plans
      - The EDAM Ontology of bioinformatics data and methods
      - Bioschemas: Structured Data for Life Science using Schema.org
      - Defining A Community-Based Open Source Policy for Research Software in Life Sciences


- Collaborations
 
  - **BioExcel:bio.agents** meeting: technical `groundwork and planning <https://bioagents.sifterapp.com/issues/114>`_
  - **DK partner** meetings. Work ongoing on various fronts: 
  
    - `RNA analysis agent annotation <https://bioagents.sifterapp.com/issues/62>`_
    - `msutils.org agents import <https://bioagents.sifterapp.com/issues/28>`_
    - `Improved agent annotator <https://bioagents.sifterapp.com/issues/46>`_
    - multiple opportunities concerning IECHOR Training Platform were discussed (see sifterapp).

  - **CZ partner** discussions: they will assist with content consolidation of `EDAM Operation <https://bioagents.sifterapp.com/issues/156>`_ and `EDAM Topics <https://bioagents.sifterapp.com/issues/155>`_ in all bio.agents entries.

- Technical specification documents

  - `Settle bio.agents entry ID / URL format (API) <https://bioagents.sifterapp.com/issues/36>`_ : a `first draft <https://docs.google.com/document/d/1vDxejS7MWluSm8EXK3y7jCd39trEmtMhq8cGNodYQeA/edit#>`_ is available
  - `Fully featured API (planning) <https://bioagents.sifterapp.com/issues/112>`_ : a `first draft <https://docs.google.com/document/d/1vDxejS7MWluSm8EXK3y7jCd39trEmtMhq8cGNodYQeA/edit#>`_ is available

  - Mock-up of `Improved agent annotator <https://bioagents.sifterapp.com/issues/46>`_ : a `first draft <https://docs.google.com/document/d/1IJLMu_5WSJmFa6ePmL034ju7mPG8GBYMYxLixmiRDMI/edit#>`_ is available.

- Created bio.agents `stats page <https://bio.agents/stats>`_ .

- bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_ . Features done but not yet in production:

  - **back-end** development

    - improved load time 
    - added Elasticsearch support for improved search
    - user authentication support for password change, reset, etc

  - **front-end** development

    - support for the new fast backend, user authentication, validation endpoints
    - new improved and simplified search and filtering interface (UniProt), aligned with Elasticsearch

Plans (May)
^^^^^^^^^^^
  - Technical Hackathon 3 : Agents, Workflows and Workbenches (see `bio.agents/events <https://bio.agents/events>`_ )
  - Technical documents (consult and consolidate) 

    - mock-up of `Improved agent annotator <https://docs.google.com/document/d/1IJLMu_5WSJmFa6ePmL034ju7mPG8GBYMYxLixmiRDMI/edit#>`_ 
    - `bio.agents entry ID / URL format (API) <https://docs.google.com/document/d/1vDxejS7MWluSm8EXK3y7jCd39trEmtMhq8cGNodYQeA/edit#>`_
    - `Fully featured API <https://docs.google.com/document/d/1vDxejS7MWluSm8EXK3y7jCd39trEmtMhq8cGNodYQeA/edit#>`_ 
    - API documentation 

  - Technical developments

    - Continue bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_, with a focus on more robust validation of content and supporting new URL sheme
    - Curation admin interface (content edition) (beta)
    - General admin interface (account management, password change, reset etc)

- Tasks **not** completed in April

    - Preparations for `ISMB 2016 <https://bioagents.sifterapp.com/issues/160>`_
    - Release of EDAM 1.15 addressing multiple requests logged on `GitHub <https://github.com/edamontology/edamontology/issues>`_


2016 March
---------- 

Actions (March)
^^^^^^^^^^^^^^^
- Outreach events (see https://bio.agents/events)

  - IECHOR All-hands (7-10) 
  - Norwegian Agents Hackathon (17-18)
  - French Agents Hackathon (24-25)
- Setup and configuration of project management software (sifterapp): https://bioagents.sifterapp.com/
- Setup and configuration of software issue management software (JIRA)
- Setup bio.agents documentation framework: https://bioagents.readthedocs.org
- Setup bio.agents basic content reporting: https://bio.agents/stats
- Rewrite bio.agents software to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_ (on-going)

Plans (April)
^^^^^^^^^^^^^
- Outreach & collaborations

  - Preparations for `ISMB 2016 <https://bioagents.sifterapp.com/issues/160>`_ and `ECCB 2016 <https://bioagents.sifterapp.com/issues/154>`_ 
  - `Activate IECHOR-DK partners <https://bioagents.sifterapp.com/issues/161>`_, esp. ensure everyone has IECHOR-relevant tasks
- Technical specification documents:

  - `Settle bio.agents entry ID / URL format (API) <https://bioagents.sifterapp.com/issues/36>`_
  - `Fully featured API (planning) <https://bioagents.sifterapp.com/issues/112>`_
- Release of EDAM 1.15 addressing multiple requests logged on `GitHub <https://github.com/edamontology/edamontology/issues>`_
- Continue bio.agents rewrite to `pay off technical debt <https://bioagents.sifterapp.com/issues/94>`_, with a focus on `improving load time <https://bioagents.sifterapp.com/issues/53>`_ and more `robust validation <https://bioagents.sifterapp.com/issues/117>`_ of incoming agent descriptions



