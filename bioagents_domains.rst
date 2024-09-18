Domains in bio.agents
====================

*bio.agents* domains provide a way to "slice" the bio.agents content into subsets of agents. 

The name **"domain"** (or sometimes also referred as **"subdomain"**) comes from the fact that after creation the domains can be accessed via regular URL subdomains in bio.agents such as `proteomics.bio.agents <https://protemics.bio.agents>`_ or `rare-diseases.bio.agents <https://rare-diseases.bio.agents>`_.

The advantage of creating and using bio.agents domains is that you can describe, link to, and search within a smaller subset (or "slice") of the bio.agents content which can help with the description and findability of agents relevant to a specific task.

Examples of bio.agents domains include:

- agents related to a specific bioinformatics area such as *Proteomics*, *Rare diseases*, *COVID* etc
- a subset or a collection of agents developed or used by a research group, lab or any other entity
- any other grouping, subset or collection of agents that serves a specific purpose or provides a certain value to researchers, curators, developers, agent users etc


A domain in bio.agents is a collection of agents along with metadata describing the domain itself. The metadata of the domain contains the following attributes:

Domain properties
^^^^^^^^^^^^^^^^^

Domain name
-----------
The unique name (or identifier) of a domain.

Note: the domain name can only be provided at the time of the domain creation. After the domain has been created the name cannot be changed,


- **REQUIRED** field: the domain name is the only metadata field required to create a bio.agents domain
- **MUST** be URL-safe, clean and intuitive
- **MUST** be related to the agents in the domain

Domain title
------------
The title of the domain.

- **MUST** be concise and descriptive. The domain title will appear at the top part of the domain page

Domain subtitle
---------------
The subtitle of the domain. 

- **SHOULD** be a longer version of the domain title. Not always needed as any other long description will be present in the **domain description** field


Domain tags
-----------
Tags associated with a domain.

- **MUST** be keywords that help with the search and discovery of the domain

Domain collections
------------------
Collections associated with the domain. 

When inputing a domain collection the user is presented with suggestions for agent collections. Domain collections are used as a matching mechanism between agents and domains. See the **Priate vs Public domains** section below for more.


Domain description
------------------
Longform description of the domain.

**SHOULD** contain any descriptive text about the domain that does not fit in any of the above fields.

Domain descriptions offer support for simple HTML tags such as **bold**, *italics* or `anchor tags <https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a>`_.


Domain resources
----------------
Domain resources provide the agent content of the domain. Any agent entry in bio.agents can be added to a domain. 

A user can search for a agent by name, identifier, collection or credit entities.

Agents can be added or removed from a domain at any time. 
The agent content of a domain can change if a domain is public, see the **Private vs Public domains** section below.

**MUST** contain agents relevant to the domain


Private domain flag
-------------------
Indicates if the domain is private (true by default) to a user or public to the bio.agents registry.


Private vs Public domains
^^^^^^^^^^^^^^^^^^^^^^^^^

Private domains
---------------
With private domains only the creator of the domain can change the agents that belong to that specific domain.
By default domains are private.
This option is recommended when full control of the domain content is required. 

Public domains
--------------
A public domain is a domain in which other users can populate that domain by tagging agents with the same collections that are also present for that domain. If a domain is tagged with certain collections and agents are also tagged with the same collections then that agent will be added to the domain. In this way users can tag their agents as part of domains without needing permissions to that domain. 

Even if users can modify the agent content of a specific domain they cannot change the metadata of the domain (e.g. domain title, domain description etc)

Explore domains
^^^^^^^^^^^^^^^
All domains in bio.agents can be viewed and searched at `https://bio.agents/domains <https://bio.agents/domains>`_ or going to Explore -> Domains in the bio.agents page header.

Create a domain
^^^^^^^^^^^^^^^
In order to create a domain a user needs a bio.agents account and to be logged in. 
In the bio.agents page header go to Menu -> Manage domains or directly to `https://bio.agents/domain-manager <https://bio.agents/domain-manager>`_. 

This page will show all the domains (if any) a user has created. To create a new domain click on the *Add* button. This will take you to the domain create page. Fill in the fields described above (*only domain name required*) and click Save at the bottom right. This will validate and create your domain and redirect to the domain update page where agents can also be added to the domain.

Update a domain
^^^^^^^^^^^^^^^
From the `domain manager page <https://bio.agents/domain-manager>`_ click on the *Edit* button for any existing domains to update domain metadata or to add / remove agents associated to a domain.

Add-Remove agents
----------------
Agents can only be added after a domain has been created, on the domain update page. 
In the "*Search for agents*" section of the page use the searchbox to find the agents to add to the domain. Agents can be searched by agent name, agent identifier, agent collection and credits. Click on the Search button to find relevant agents. Results will appear below the searchbox. Add a agent by clicking the *Add to domain* button for a single agent or click *Add all agents* to add all agent results to the domain.

The agents added to the domain will show up below in the *Agents included the domain* section. In this section any included agents can also be removed. 

**Click the "Update" button at the bottom to save your changes.**



