***************
API Usage Guide
***************

.. attention::

   - guidelines for the `bio.agents <https://bio.agents>`_ API 
   - to make suggestions about these guidelines please add comments via `GitHub <https://github.com/bio-agents/bioagentsDocs/issues/>`_
   - see also the `API Reference <https://bioagents.readthedocs.io/en/latest/api_reference.html>`_  

bio.agents implements the model of software information defined in `bioagentsScheme v3.0.0 <https://github.com/bio-agents/bioagents schema>`_ .  This page summarises the structure and syntax of an XML / JSON file that describes a agent for submission to bio.agents via the API.


Payload formats
===============
To submit a agent via the bio.agents API you’ll need to POST a agent description to the `agent endpoint <http://bioagents.readthedocs.io/en/latest/api_reference.html#register-a-resource>`_. The API supports XML and JSON format uploads and downloads comatible with `bioagents schema <https://github.com/bio-agents/bioagents-schema>`_.


.. note::
   Support for YAML (and other) formats can be added if required.  If you want this, please tell us via `GitHub <https://github.com/bio-agents/bioagentsregistry/issues>`_.

 
XML
---
See the `sample XML document <https://github.com/bio-agents/bioagents schema/tree/master/stable/example_files>`_.


.. important::
   When working in XML, please first read the `bioagents schema docs <https://bioagents-schema.readthedocs.io/en/latest/bioagents-schema_elements.html>`_.  It is essential to stick to the element order (including nested elements) in the `sample XML documents <https://github.com/bio-agents/bioagents schema/tree/master/stable/example_files>`_ and as shown below.


JSON
----

A sample JSON document may look like this:

.. code-block:: js

   {
      "name": "SignalP",
      "description": "Prediction of the presence and location of signal peptide cleavage sites in amino acid sequences from different organisms.",
      "homepage": "http://cbs.dtu.dk/services/SignalP/",
      "bioagentsID": "signalp",
      "bioagentsCURIE": "bioagents:signalp",
      "version":
      [
         "6.4.0.0",
         "1.1 - 1.4, 2.0-alpha, 2.0-beta-01 - 2.0-beta-04, 2.0.0"
      ]
      "otherID":
      [
         {
            "value": "RRID:SCR_015644",
	    "type": "rrid",
            "version": "4.1"
         },
         {
            "value": "doi:10.1007/978-1-4939-7015-5_6",
            "type": "doi"
            "version": "4.1"	    
         }
      ]
     
      "function":
      [
         {
            "operation":
	    [
               {
                  "uri": "http://edamontology.org/operation_0418",
                  "term": "Protein signal peptide detection"
               },
               {
                  "uri": "http://edamontology.org/operation_0422",
                  "term": "Protein cleavage site prediction"
               }
            ],
            "input":
	    [
              {
                "data":
	        {
                   "uri": "http://edamontology.org/data_2044",
                   "term": "Sequence"
                },
                "format":
	        [
                  {
                     "uri": "http://edamontology.org/format_1929",
                     "term": "FASTA"
                  },
                  {
                     "uri": "http://edamontology.org/format_3008",
                     "term": "MAF"
                  }
                ]
              }
            ],
            "output":
	    [
               {
                  "data":
	          {
                     "uri": "http://edamontology.org/data_1277",
                     "term": "Protein features"
                  },
                  "format":
	          [
                     {
                        "uri": "http://edamontology.org/format_2305",
                        "term": "GFF"
                     },
		                          {
                        "uri": "http://edamontology.org/format_3164",
                        "term": "GTrack"
                     },
                  ]
               },
               {
                  "data":
	          {
                     "uri": "http://edamontology.org/data_2955",
                     "term": "Sequence report"
                  },
                  "format":
	          [
              	     {
                        "uri": "http://edamontology.org/format_2331",
                        "term": "HTML"
                     }
                  ]
               }
            ]
            "note": "Predicts the presence and location of signal peptide cleavage sites in amino acid sequences from different organisms.",
            "cmd": "--someOption",
         }  
      ],
      "agentType":
      [
        "Command-line agent",
        "Web application"
      ],
      "topic":
      [
        {
          "uri": "http://edamontology.org/topic_0080",
          "term": "Sequence analysis"
        },
        {
          "uri": "http://edamontology.org/topic_0078",
          "term": "Proteins"
        }
      ],
      "operatingSystem":
      [
        "Linux",
        "Mac"
      ],
      "language":
      [
        "ActionScript",
        "C"
      ],
      "license": "Proprietary",
      "collectionID":
      [
        "CBS",
        "myagents"
      ],
      "maturity": "Mature",
      "cost": "Free of charge (with restrictions)",
      "accessibility":
      [
         "Open access",
      ],
      "link":
      [
        {
          "url": "http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp",
          "type": "Repository",
          "note": "A comment goes here"
        },
        {
          "url": "http://www.cbs.dtu.dk/helpdesk",
          "type": "Helpdesk",
          "type": "Issue tracker",
          "note": "A comment goes here"
        }
      ],
      "download":
      [
        {
          "url": "http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp",
          "type": "Source code",
          "note": "A comment goes here"
          "version": "1.4"
      },
        {
          "url": "http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp",
          "type": "Binaries",
          "note": "A comment goes here"
          "version": "1.4"
        }
      ],
      "documentation":
      [
        {
          "url": "http://www.cbs.dtu.dk/services/SignalP",
          "type": "General",
          "type": "Code of conduct",
          "note": "A comment goes here"
        },
       {
          "url": "http://www.cbs.dtu.dk/services/SignalP",
          "type": "Citation instructions",
          "note": "A comment goes here"
        }
      ],
      "relation":
      [
        {
          "bioagentsID": "needle",
          "type": "isNewVersionOf",
        },
       {
          "bioagentsID": "emboss",
          "type": "includedIn"
        }
      ],
      "publication":
      [
        {
           "doi": "10.1038/nmeth.1701",
           "pmid": "21959131",
           "pmcid": "21959131",
           "type": "Primary",
           "note": "A comment goes here",
           "version": "1.4"
        },
        {
           "doi": "10.1038/nmeth.1701",
           "pmid": "21959131",
           "pmcid": "21959131",
           "type": "Other",
           "note": "A comment goes here",
           "version": "1.4"
        }
      ],
      "credit":
      [
         {
            "name": "TN Petersen",
            "email": "test@email.com",
            "url": "http://someurl.org",
            "orcidid": "test",
            "gridid": "test",
            "rorid": "test",
            "fundrefid": "test",	 
            "typeEntity": "Person",
            "typeRole": "Developer",
            "note": "A comment goes here"
         },
 	 {
 	    "iechorPlatform", "Agents",
 	 },
  	 {
 	    "iechorNode", "Denmark"
         }
      ],
    }

    
Agent attributes
===============


Name
----
*Canonical software name assigned by the software developer or service provider, e.g. "needle"*

Attribute name
  name

Required
  Yes

Cardinality
  1 only
  
Type
  String

Restrictions
  Min length: 1

  Max length: 100

  Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``

**Example**

.. code-block:: js
		
  # XML
  <name>needle</name>

  # JSON
  "name": "needle"





.. note::
   - name may only contain space, uppercase and lowercase letters, decimal digits, plus symbol, period, comma, dash, underscore, colon, semicolon and parentheses.
   - line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#name-agent>`_.


Description
-----------
*Textual description of the software, e.g. "needle reads two input sequences and writes their optimal global sequence alignment to file. It uses the Needleman-Wunsch alignment algorithm to find the optimum alignment (including gaps) of two sequences along their entire length. The algorithm uses a dynamic programming method to ensure the alignment is optimum, by exploring all possible alignments and choosing the best."*

Attribute name
  description

Required
  Yes

Cardinality
  1 only

Type
  String

Restrictions
  Min length: 10
  
  Max length: 1000

**Example**

.. code-block:: js

  # XML
  <description>needle reads two input sequences and writes their optimal global sequence alignment to file. It uses the Needleman-Wunsch alignment algorithm to find the optimum alignment (including gaps) of two sequences along their entire length. The algorithm uses a dynamic programming method to ensure the alignment is optimum, by exploring all possible alignments and choosing the best.</description>

  # JSON
  "description": "needle reads two input sequences and writes their optimal global sequence alignment to file. It uses the Needleman-Wunsch alignment algorithm to find the optimum alignment (including gaps) of two sequences along their entire length. The algorithm uses a dynamic programming method to ensure the alignment is optimum, by exploring all possible alignments and choosing the best."

.. note::
  - minimum 10 and maximum 1000 characters.
  - line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
  - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#description>`_.


Homepage
--------
*Homepage of the software, or some URL that best serves this purpose, e.g. "http://emboss.open-bio.org/rel/rel6/apps/needle.html"*

Attribute name
  homepage

Required
  Yes

Cardinality
  1
  
Type
  URL

Restrictions
  Pattern: ``http(s?)://[^\s/$.?#].[^\s]*``

**Example**

.. code-block:: js

  # XML
  <homepage>http://emboss.open-bio.org/rel/rel6/apps/needle.html</homepage>

  # JSON
  "homepage": "http://emboss.open-bio.org/rel/rel6/apps/needle.html"

.. note::
   - a single valid URL is specified.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#homepage>`_.


bioagentsID
----------
*Unique ID (case insensitive) of the agent that is assigned upon registration of the software in bio.agents, normally identical to agent name, e.g. "needle".*

Attribute name
  bioagentsID

Required
  No

Cardinality
  0 or 1
  
Type
  String

Restrictions
  Pattern: ``[_\-.0-9a-zA-Z]*``

**Example**

.. code-block:: js

  # XML
  <bioagentsID>needle</bioagentsID>

  # JSON
  "bioagentsID": "needle"

.. attention::
   - a bioagentsID is set (and can only be changed) by bio.agents admin.  It can be retrieved by API, but if specified in the payload to a ``PUT`` or ``POST`` request will be disregarded.  
     
.. note::
   - the bioagentssID is a URL-safe and Linked-Data-safe derivative of (often identical to) the agent name. Allowed characters are uppercase and lowercase English letters (case insensitive!), decimal digits, hyphen, period, and underscore. Spaces can be preserved as underscore ("_").
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#bioagentsid>`_.


bioagentsCURIE
-------------
*bio.agents CURIE (compact URI) based on the unique bio.agents ID of the agent, e.g. "bioagents:needle"*

Attribute name
  bioagentsCURIE

Required
  No

Cardinality
  0 or 1
  
Type
  String

Restrictions
  Pattern: ``bioagents:[_\-.0-9a-zA-Z]*``

**Example**

.. code-block:: js

  # XML
  <bioagentsCURIE>needle</bioagentsCURIE>

  # JSON
  "bioagentsCURIE": "needle"

.. attention::
   - a bioagentsCURIE is set (and can only be changed) by bio.agents admin.  It can be retrieved by API, but if specified in the payload to a ``PUT`` or ``POST`` request will be disregarded.
   
.. note::
   - the bio.agents CURIE is simply the bio.agents agent ID with the prefix "bioagents:".
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#bioagentscurie>`_.


Version
-------
*Version information (typically a version number) of the software applicable to this bio.agents entry, e.g. "6.4.0.0"*

Attribute name
 version

Required
  No

Cardinality
  0 to many
  
Type
  String array

Restrictions
  Min length: 1

  Max length: 100

  Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``
  
**Example**

.. code-block:: js

  # XML
  <version>6.4.0.0</version>
  <version>1.1 - 1.4, 2.0-alpha, 2.0-beta-01 - 2.0-beta-04, 2.0.0</version>
  
  # JSON
  "version":
  [
    "6.4.0.0",
    "1.1 - 1.4, 2.0-alpha, 2.0-beta-01 - 2.0-beta-04, 2.0.0"
  ]


.. note::
   - name may only contain space, uppercase and lowercase English letters, decimal digits, plus symbol, period, comma, dash, colon, semicolon and parentheses.
   - line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#version>`_.
     
  
Other IDs
---------
*A unique identifier of the software, typically assigned by an ID-assignment authority other than bio.agents, e.g. "RRID:SCR_015644"*

Attribute name
  otherID

Required
  No

Cardinality
  0 to many
  
Type
  List of otherID objects

otherID object definition
  * value
      * Required: Yes
      * Cardinality: 1 only
      * Type: String
      * Pattern: ``(doi|DOI):?10.[0-9]{4,9}[A-Za-z0-9:;\)\(_/.-]+``
      * Pattern: ``(rrid|RRID):.+``
      * Pattern: ``(cpe|CPE):.+``
      * Pattern: ``(bioagents|BIOTOOLS):[_\-.0-9a-zA-Z]*``
      
  * type
      * Required: No
      * Cardinality: 0 or 1
      * Type: ENUM (list)
      * Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#other-ids>`_)
	
        - ``doi``
        - ``rrid``
        - ``cpe``
        - ``bioagentsCURIE``
	  
  * version
      * Required: No
      * Cardinality: 0 or 1
      * Type: String
      * Restrictions: Min length: 1, Max length: 100
      *	Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``

**Example**

.. code-block:: js

  # XML
  <otherID>
        <value>RRID:SCR_015644</value>
        <type>rrid</type>
        <version>4.1</version>
  </otherID>
  <otherID>
        <value>doi:10.1007/978-1-4939-7015-5_6</value>
        <type>doi</type>
        <version>4.1</version>
  </otherID>
			
  # JSON		
  "otherID":
  [
        {
            "value": "RRID:SCR_015644",
	    "type:" "rrid",
            "version": "4.1"
        },
        {
            "value": "doi:10.1007/978-1-4939-7015-5_6",
            "type": "doi"
            "version": "4.1"	    
        }
  ]

.. note::
   - type can normally be inferred from the value but should be specified otherwise.  In the example it was not actually necessary to specify "type".
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#other-ids>`_.

.. _function:

Function
--------
*Details of a function (i.e. mode of operation) the software provides, expressed in terms from the EDAM ontology.*

Attribute name
  function

Required
  No

Cardinality
  0 to many
  
Type
  List of function objects

Function object definition
  Content
    * :ref:`operation`
        * Required: Yes
	* Cardinality: 1 to many
        * Type: List of EDAM objects
    * :ref:`input`
        * Required: No
	* Cardinality: 0 to many
        * Type: List of input objects
    * :ref:`output`
        * Required: No
	* Cardinality: 0 to many
        * Type: List of output objects
    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 10, max length: 1000
    * cmd
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 1, max length: 1000

.. note::
   - **note** and **cmd**: line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the curation guidelines for the `function group <http://bioagents.readthedocs.io/en/latest/curators_guide.html#function-group>`_, `note <http://bioagents.readthedocs.io/en/latest/curators_guide.html#note>`_ and `command <http://bioagents.readthedocs.io/en/latest/curators_guide.html#command>`_.
	  
**Example**

.. code-block:: js

  # XML
  <function>
      <operation>
          <uri>http://edamontology.org/operation_0418</uri>
          <term>Protein signal peptide detection</term>
      </operation>
      <operation>
          <uri>http://edamontology.org/operation_0422</uri>
          <term>Protein cleavage site prediction</term>
      </operation>
      <input>
          <data>
            <uri>http://edamontology.org/data_2044</uri>
            <term>Sequence</term>
          </data>
          <format>
              <uri>http://edamontology.org/format_1929</uri>
              <term>FASTA</term>
          </format>
      <output>
          <data>
            <uri>http://edamontology.org/data_1277</uri>
            <term>Protein features</term>
          </data>
          <format>
              <uri>http://edamontology.org/format_2305</uri>
              <term>GFF</term>
          </format>
          <data>
            <uri>http://edamontology.org/data_2955</uri>
            <term>Sequence report</term>
          </data>
          <format>
              <uri>http://edamontology.org/format_1929</uri>
              <term>FASTA</term>
          </format>
      </output>
      <note>Predicts the presence and location of signal peptide cleavage sites in amino acid sequences from different organisms.</note>
      <cmd>-s best</cmd>
  </function>  


  # JSON
  "function":
  [
    {
      "operation":
      [
        {
          "uri": "http://edamontology.org/operation_0418",
          "term": "Protein signal peptide detection"
        },
        {
          "uri": "http://edamontology.org/operation_0422",
          "term": "Protein cleavage site prediction"
        }
      ],
      "input":
      [
        {
          "data":
	  {
            "uri": "http://edamontology.org/data_2044",
            "term": "Sequence"
          },
          "format":
	  [
            {
              "uri": "http://edamontology.org/format_1929",
              "term": "FASTA"
            }
          ]
        }
      ],
      "output":
      [
        {
          "data":
	  {
            "uri": "http://edamontology.org/data_1277",
            "term": "Protein features"
          },
          "format":
	  [
            {
              "uri": "http://edamontology.org/format_2305",
              "term": "GFF"
            }
          ]
        },
        {
          "data":
	  {
            "uri": "http://edamontology.org/data_2955",
            "term": "Sequence report"
          },
          "format":
	  [
            {
              "uri": "http://edamontology.org/format_1929",
              "term": "FASTA"
            }
          ]
        }
      ]
      "note": "Predicts the presence and location of signal peptide cleavage sites in amino acid sequences from different organisms.",
      "cmd": "-s best",
    }
  ]

.. _operation:

Operation
.........
*The basic operation(s) performed by this software function (EDAM Operation), e.g. "'Protein signal peptide detection' (http://edamontology.org/operation_0418)"*

Attribute name
  operation

Required
  Yes 

Cardinality
  1 to many
  
Child of
  :ref:`function`

Type
  List of EDAM objects

EDAM object definition
  Content
    * uri
        * Required: No (if term present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: URL
    * term
        * Required: No (if URI present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: String

.. note::
   - an `EDAM ontology <https://github.com/edamontology/edamontology>`_ Operation concept URL and / or term are specified, *e.g.* "Multiple sequence alignment", http://edamontology.org/operation_0492.
   - URI and term are validated against EDAM ontology; if term and URI do not match, an error will be returned.
   - synonyms of terms (as defined in EDAM) are accepted
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#operation>`_.


**Example**

.. code-block:: js

  # XML
  <operation>
          <uri>http://edamontology.org/operation_0418</uri>
          <term>Protein signal peptide detection</term>
  </operation>
  <operation>
          <uri>http://edamontology.org/operation_0422</uri>
          <term>Protein cleavage site prediction</term>
  </operation>
  
  # JSON		
  "operation":
  [
      {
          "uri": "http://edamontology.org/operation_0418",
          "term": "Protein signal peptide detection"
      },
      {
          "uri": "http://edamontology.org/operation_0422",
          "term": "Protein cleavage site prediction"
      }
  ]

.. _input:

Input
.....
*Primary input data (if any)*

Attribute name
  input

Required
  No

Cardinality
  0 to many
  
Child of
  :ref:`function`

Type
  List of input objects

Input object definition
  Content
    * data
        * Required: Yes
	* Cardinality: 1 only
        * Type: EDAM object
    * format
        * Required: No
	* Cardinality: 0 to many
        * Type: List of EDAM objects

**Example**

.. code-block:: js

  # XML
      <data>
        <uri>http://edamontology.org/data_2044</uri>
        <term>Sequence</term>
      </data>
      <format>
          <uri>http://edamontology.org/format_1929</uri>
          <term>FASTA</term>
      </format>
  
  # JSON
  "input":
  [
    {
      "data":
      {
        "uri": "http://edamontology.org/data_2044",
        "term": "Sequence"
      },
      "format":
      [
        {
          "uri": "http://edamontology.org/format_1929",
          "term": "FASTA"
        }
      ]
    }
  ]

.. _output:

Output
......
*Primary output data (if any)*

Attribute name
  output

Required
  No

Cardinality
  0 to many
  
Child of
  :ref:`function`

Type
  List of output objects

Output object definition
  Content
    * data
        * Required: Yes
	* Cardinality: 1 only
        * Type: EDAM object
    * format
        * Required: No
	* Cardinality: 0 to many
        * Type: List of EDAM objects

**Example**

.. code-block:: js

  # XML
  "output":
      <data>
        <uri>http://edamontology.org/data_2044</uri>
        <term>Sequence</term>
      </data>
      <format>
          <uri>http://edamontology.org/format_1929</uri>
          <term>FASTA</term>
      </format>
  
  # JSON
  "output":
  [
    {
      "data":
      {
        "uri": "http://edamontology.org/data_2044",
        "term": "Sequence"
      },
      "format":
      [
        {
          "uri": "http://edamontology.org/format_1929",
          "term": "FASTA"
        }
      ]
    }
  ]

.. _data:

Data
....
*EDAM Data concept,  e.g. "'Sequence' (http://edamontology.org/data_2044)"*
Attribute name
  data

Required
  Yes

Cardinality
  1 only
  
Child of
  :ref:`input` or :ref:`output`

Type
  EDAM object

EDAM object definition
  Content
    * uri
        * Required: No (if term present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: URL
    * term
        * Required: No (if URI present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: String

.. note::
   - an `EDAM ontology <https://github.com/edamontology/edamontology>`_ Data concept URL and / or term are specified, *e.g.* "Protein sequences", http://edamontology.org/data_2976. 
   - URI and term are validated against EDAM ontology; if term and URI do not match, an error will be returned.
   - synonyms of terms (as defined in EDAM) are accepted, however, **the synonym will be replaced with main term**.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#data-type-input-and-output-data>`_.

**Example**

.. code-block:: js

  # XML
  <data>
   <uri>http://edamontology.org/data_2044</uri>
   <term>Sequence</term>
  </data>
  
  # JSON		
  "data":
  {
    "uri": "http://edamontology.org/data_2044",
    "term": "Sequence"
  }

.. _format:

Format
......
*EDAM Format concept,  e.g. "'FASTA' (http://edamontology.org/format_1929)"*

Attribute name
  format

Required
  No

Cardinality
  0 to many
  
Child of
  :ref:`input` or :ref:`output`

Type
  List of EDAM objects

EDAM object definition
  Content
    * uri
        * Required: No (if term present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: URL
    * term
        * Required: No (if URI present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: String

.. note::
   - an `EDAM ontology <https://github.com/edamontology/edamontology>`_ Format concept URL and / or term are specified, *e.g.* "FASTA", http://edamontology.org/format_1929.
   - URI and term are validated against EDAM ontology; if term and URI do not match, an error will be returned.
   - synonyms of terms (as defined in EDAM) are accepted, however, **the synonym will be replaced with main term**.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#data-format-input-and-output-data>`_.


**Example**

.. code-block:: js

  # XML
  <format>
   <uri>http://edamontology.org/format_1929</uri>
   <term>FASTA</term>
  </format>
  
  # JSON		
  "format":
  [
    {
      "uri": "http://edamontology.org/format_1929",
      "term": "FASTA"
    }
  ]


Agent type
---------
*The type of application software: a discrete software entity can have more than one type, e.g. "Command-line agent, Web application"*

Attribute name
  agentType

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#agent-type>`_)
  - ``Bioinformatics portal``
  - ``Command-line agent``
  - ``Database portal``
  - ``Desktop application``
  - ``Library``
  - ``Ontology``
  - ``Plug-in``
  - ``Script``
  - ``SPARQL endpoint``
  - ``Suite``
  - ``Web application``
  - ``Web API``
  - ``Web service``
  - ``Workbench``
  - ``Workflow``

**Example**

.. code-block:: js

  # XML
  <agentType>Command-line agent</agentType>
  <agentType>Web application</agentType>
    
  # JSON
  "agentType":
  [
    "Command-line agent",
    "Web application"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#agent-type>`_.

  
Topic
-----
*General scientific domain the software serves or other general category (EDAM Topic), e.g. "'Protein sites, features and motifs' (http://edamontology.org/topic_3510)"*

Attribute name
  topic

Required
  No

Cardinality
  0 to many
  
Type
  List of EDAM objects

EDAM object definition
  Content
    * uri
        * Required: No (if term present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: URL
    * term
        * Required: No (if URI present), Yes (otherwise)
	* Cardinality: 0 or 1
        * Type: String

**Example**

.. code-block:: js

  # XML
  <topic>
    <uri>http://edamontology.org/topic_0605</uri>
    <term>Informatics</term>
  </topic>
  <topic>
    <uri>http://edamontology.org/topic_3303</uri>
    <term>Medicine</term>
  </topic>
    
  # JSON		
  "topic":
  [
    {
      "uri": "http://edamontology.org/topic_0605",
      "term": "Informatics"
    },
    {
      "uri": "http://edamontology.org/topic_3303",
      "term": "Medicine"
    }
  ]

.. note::
   - an `EDAM ontology <https://github.com/edamontology/edamontology>`_ Topic concept URL and / or term are specified, *e.g.* "Proteomics", http://edamontology.org/topic_0121.
   - URI and term are validated against EDAM ontology; if term and URI do not match, an error will be returned.
   - synonyms of terms (as defined in EDAM) are accepted, however, **the synonym will be replaced with main term**.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#topic>`_.

Operating system
----------------
*The operating system supported by a downloadable software package, e.g. "Linux"*

Attribute name
  operatingSystem

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#operating-system>`_)
  - ``Linux``
  - ``Windows``
  - ``Mac``

**Example**

.. code-block:: js

  # XML
  <operatingSystem>Linux</operatingSystem>
  <operatingSystem>Mac</operatingSystem>
    
  # JSON		
  "operatingSystem":
  [
    "Linux",
    "Mac"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#operating-system>`_.

     
Programming language
--------------------
*Name of programming language the software source code was written in, e.g. "C"*

Attribute name
  language

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#programming-language>`_)
  ``ActionScript``, ``Ada``, ``AppleScript``, ``Assembly language``, ``AWK``, ``Bash``, ``C``, ``C#``, ``C++``, ``COBOL``, ``ColdFusion``, ``CWL``, ``D``, ``Delphi``, ``Dylan``, ``Eiffel``, ``Forth``, ``Fortran``, ``Groovy``, ``Haskell``, ``Icarus``, ``Java``, ``JavaScript``, ``Julia``, ``JSP``, ``LabVIEW``, ``Lisp``, ``Lua``, ``Maple``, ``Mathematica``, ``MATLAB``, ``MLXTRAN``, ``NMTRAN``, ``OCaml``, ``Pascal``, ``Perl``, ``PHP``, ``Prolog``, ``PyMOL``, ``Python``, ``R``, ``Racket``, ``REXX``, ``Ruby``, ``SAS``, ``Scala``, ``Scheme``, ``Shell``, ``Smalltalk``, ``SQL``, ``Turing``, ``Verilog``, ``VHDL``, ``Visual Basic``, ``XAML``, ``Other``

**Example**

.. code-block:: js

  # XML
  <language>Python</language>
  <language>C</language>

  # JSON		
  "language":
  [
    "Python",
    "C"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#language>`_.

License
-------
*Software or data usage license, e.g. "GPL-3.0"*

Attribute name
  license

Required
  No

Cardinality
  0 or 1
 
Type
  ENUM

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#license>`_)
  ``0BSD``, ``AAL``, ``ADSL``, ``AFL-1.1``, ``AFL-1.2``, ``AFL-2.0``, ``AFL-2.1``, ``AFL-3.0``, ``AGPL-1.0``, ``AGPL-3.0``, ``AMDPLPA``, ``AML``, ``AMPAS``, ``ANTLR-PD``, ``APAFML``, ``APL-1.0``, ``APSL-1.0``, ``APSL-1.1``, ``APSL-1.2``, ``APSL-2.0``, ``Abstyles``, ``Adobe-2006``, ``Adobe-Glyph``, ``Afmparse``, ``Aladdin``, ``Apache-1.0``, ``Apache-1.1``, ``Apache-2.0``, ``Artistic-1.0``, ``Artistic-1.0-Perl``, ``Artistic-1.0-cl8``, ``Artistic-2.0``, ``BSD-2-Clause``, ``BSD-2-Clause-FreeBSD``, ``BSD-2-Clause-NetBSD``, ``BSD-3-Clause``, ``BSD-3-Clause-Attribution``, ``BSD-3-Clause-Clear``, ``BSD-3-Clause-LBNL``, ``BSD-3-Clause-No-Nuclear-License``, ``BSD-3-Clause-No-Nuclear-License-2014``, ``BSD-3-Clause-No-Nuclear-Warranty``, ``BSD-4-Clause``, ``BSD-4-Clause-UC``, ``BSD-Protection``, ``BSD-Source-Code``, ``BSL-1.0``, ``Bahyph``, ``Barr``, ``Beerware``, ``BitTorrent-1.0``, ``BitTorrent-1.1``, ``Borceux``, ``CATOSL-1.1``, ``CC-BY-1.0``, ``CC-BY-2.0``, ``CC-BY-2.5``, ``CC-BY-3.0``, ``CC-BY-4.0``, ``CC-BY-NC-1.0``, ``CC-BY-NC-2.0``, ``CC-BY-NC-2.5``, ``CC-BY-NC-3.0``, ``CC-BY-NC-4.0``, ``CC-BY-NC-ND-1.0``, ``CC-BY-NC-ND-2.0``, ``CC-BY-NC-ND-2.5``, ``CC-BY-NC-ND-3.0``, ``CC-BY-NC-ND-4.0``, ``CC-BY-NC-SA-1.0``, ``CC-BY-NC-SA-2.0``, ``CC-BY-NC-SA-2.5``, ``CC-BY-NC-SA-3.0``, ``CC-BY-NC-SA-4.0``, ``CC-BY-ND-1.0``, ``CC-BY-ND-2.0``, ``CC-BY-ND-2.5``, ``CC-BY-ND-3.0``, ``CC-BY-ND-4.0``, ``CC-BY-SA-1.0``, ``CC-BY-SA-2.0``, ``CC-BY-SA-2.5``, ``CC-BY-SA-3.0``, ``CC-BY-SA-4.0``, ``CC0-1.0``, ``CDDL-1.0``, ``CDDL-1.1``, ``CECILL-1.0``, ``CECILL-1.1``, ``CECILL-2.0``, ``CECILL-2.1``, ``CECILL-B``, ``CECILL-C``, ``CNRI-Jython``, ``CNRI-Python``, ``CNRI-Python-GPL-Compatible``, ``CPAL-1.0``, ``CPL-1.0``, ``CPOL-1.02``, ``CUA-OPL-1.0``, ``Caldera``, ``ClArtistic``, ``Condor-1.1``, ``Crossword``, ``CrystalStacker``, ``Cube``, ``D-FSL-1.0``, ``DOC``, ``DSDP``, ``Dotseqn``, ``ECL-1.0``, ``ECL-2.0``, ``EFL-1.0``, ``EFL-2.0``, ``EPL-1.0``, ``EUDatagrid``, ``EUPL-1.0``, ``EUPL-1.1``, ``Entessa``, ``ErlPL-1.1``, ``Eurosym``, ``FSFAP``, ``FSFUL``, ``FSFULLR``, ``FTL``, ``Fair``, ``Frameworx-1.0``, ``FreeImage``, ``GFDL-1.1``, ``GFDL-1.2``, ``GFDL-1.3``, ``GL2PS``, ``GPL-1.0``, ``GPL-2.0``, ``GPL-3.0``, ``Giftware``, ``Glide``, ``Glulxe``, ``HPND``, ``HaskellReport``, ``IBM-pibs``, ``ICU``, ``IJG``, ``IPA``, ``IPL-1.0``, ``ISC``, ``ImageMagick``, ``Imlib2``, ``Info-ZIP``, ``Intel``, ``Intel-ACPI``, ``Interbase-1.0``, ``JSON``, ``JasPer-2.0``, ``LAL-1.2``, ``LAL-1.3``, ``LGPL-2.0``, ``LGPL-2.1``, ``LGPL-3.0``, ``LGPLLR``, ``LPL-1.0``, ``LPL-1.02``, ``LPPL-1.0``, ``LPPL-1.1``, ``LPPL-1.2``, ``LPPL-1.3a``, ``LPPL-1.3c``, ``Latex2e``, ``Leptonica``, ``LiLiQ-P-1.1``, ``LiLiQ-R-1.1``, ``LiLiQ-Rplus-1.1``, ``Libpng``, ``MIT``, ``MIT-CMU``, ``MIT-advertising``, ``MIT-enna``, ``MIT-feh``, ``MITNFA``, ``MPL-1.0``, ``MPL-1.1``, ``MPL-2.0``, ``MPL-2.0-no-copyleft-exception``, ``MS-PL``, ``MS-RL``, ``MTLL``, ``MakeIndex``, ``MirOS``, ``Motosoto``, ``Multics``, ``Mup``, ``NASA-1.3``, ``NBPL-1.0``, ``NCSA``, ``NGPL``, ``NLOD-1.0``, ``NLPL``, ``NOSL``, ``NPL-1.0``, ``NPL-1.1``, ``NPOSL-3.0``, ``NRL``, ``NTP``, ``Naumen``, ``NetCDF``, ``Newsletr``, ``Nokia``, ``Noweb``, ``Nunit``, ``OCCT-PL``, ``OCLC-2.0``, ``ODbL-1.0``, ``OFL-1.0``, ``OFL-1.1``, ``OGTSL``, ``OLDAP-1.1``, ``OLDAP-1.2``, ``OLDAP-1.3``, ``OLDAP-1.4``, ``OLDAP-2.0``, ``OLDAP-2.0.1``, ``OLDAP-2.1``, ``OLDAP-2.2``, ``OLDAP-2.2.1``, ``OLDAP-2.2.2``, ``OLDAP-2.3``, ``OLDAP-2.4``, ``OLDAP-2.5``, ``OLDAP-2.6``, ``OLDAP-2.7``, ``OLDAP-2.8``, ``OML``, ``OPL-1.0``, ``OSET-PL-2.1``, ``OSL-1.0``, ``OSL-1.1``, ``OSL-2.0``, ``OSL-2.1``, ``OSL-3.0``, ``OpenSSL``, ``PDDL-1.0``, ``PHP-3.0``, ``PHP-3.01``, ``Plexus``, ``PostgreSQL``, ``Python-2.0``, ``QPL-1.0``, ``Qhull``, ``RHeCos-1.1``, ``RPL-1.1``, ``RPL-1.5``, ``RPSL-1.0``, ``RSA-MD``, ``RSCPL``, ``Rdisc``, ``Ruby``, ``SAX-PD``, ``SCEA``, ``SGI-B-1.0``, ``SGI-B-1.1``, ``SGI-B-2.0``, ``SISSL``, ``SISSL-1.2``, ``SMLNJ``, ``SMPPL``, ``SNIA``, ``SPL-1.0``, ``SWL``, ``Saxpath``, ``Sendmail``, ``SimPL-2.0``, ``Sleepycat``, ``Spencer-86``, ``Spencer-94``, ``Spencer-99``, ``SugarCRM-1.1.3``, ``TCL``, ``TMate``, ``TORQUE-1.1``, ``TOSL``, ``UPL-1.0``, ``Unicode-TOU``, ``Unlicense``, ``VOSTROM``, ``VSL-1.0``, ``Vim``, ``W3C``, ``W3C-19980720``, ``WTFPL``, ``Watcom-1.0``, ``Wsuipa``, ``X11``, ``XFree86-1.1``, ``XSkat``, ``Xerox``, ``Xnet``, ``YPL-1.0``, ``YPL-1.1``, ``ZPL-1.1``, ``ZPL-2.0``, ``ZPL-2.1``, ``Zed``, ``Zend-2.0``, ``Zimbra-1.3``, ``Zimbra-1.4``, ``Zlib``, ``bzip2-1.0.5``, ``bzip2-1.0.6``, ``curl``, ``diffmark``, ``dvipdfm``, ``eGenix``, ``gSOAP-1.3b``, ``gnuplot``, ``iMatix``, ``libtiff``, ``mpich2``, ``psfrag``, ``psutils``, ``xinetd``, ``xpp``, ``zlib-acknowledgement``, ``Proprietary``, ``Freeware``, ``Other``, ``Not licensed``

**Example**

.. code-block:: js

  # XML
  <license>Proprietary</license>
  
  # JSON		
  "license": "Proprietary"

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#license>`_.
  
Collection
----------
*Unique ID of a collection that the software has been assigned to within bio.agents, e.g. "CBS*

Attribute name
  collectionID

Required
  No

Cardinality
  0 to many

Type
  List of strings

Restrictions
  Min length: 1

  Max length: 100

  Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``
    
**Example**

.. code-block:: js

  # XML
  <collectionID>CBS</collectionID>
  <collectionID>NorduGrid</collectionID>
  
  # JSON		
  "collectionID":
  [
    "CBS",
    "NorduGrid"
  ]

.. note::
   - collection may only contain space, uppercase and lowercase letters, decimal digits, plus symbol, period, comma, dash, underscore, colon, semicolon and parentheses.
   - line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#collection>`_.

  

Maturity
--------
*How mature the software product is, e.g. "Mature"*

Attribute name
  maturity

Required
  No

Cardinality
  0 or 1
  
Type
  ENUM

Allowed valuse (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#maturity>`_)
  - ``Emerging``
  - ``Mature``
  - ``Legacy``

**Example**

.. code-block:: js

  # XML
  <maturity>Mature</maturity>
  
  # JSON		
  "maturity": "Mature"

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#maturity>`_.  
  
Cost
----
*Monetary cost of acquiring the software, e.g. "Free of charge (with retritions)"*

Attribute name
  cost

Required
  No

Cardinality
  0 or 1
  
Type
  ENUM

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#cost>`_)
  - ``Free of charge``
  - ``Free of charge (with restrictions)``
  - ``Commercial``

**Example**

.. code-block:: js

  # XML
  <cost>Free of charge (with restrictions)</cost>
  
  # JSON		
  "cost": "Free of charge (with restrictions)"

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#cost>`_.

Accessibility
-------------
*Whether there are non-monetary restrictions on accessing an online service, e.g. "Open access"*

Attribute name
  accessibility

Required
  No

Cardinality
  0 or 1
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#accessibility>`_)
  - ``Open access``
  - ``Open access (with restrictions)``    
  - ``Restricted access``

    
**Example**

.. code-block:: js

  # XML
  <accessibility>Open access</accessibility>
  
  # JSON		
  "accessibility":
  [
    "Open access",
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#accessibility>`_.


IECHOR platform
---------------
*IECHOR platform credited for developing or providing the software.*

Attribute name
  iechorPlatform

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-platform>`_)

  - ``Data``
  - ``Agents``
  - ``Compute``
  - ``Interoperability``
  - ``Training``

**Example**

.. code-block:: js

  # XML
  <iechorPlatform>Open access</iechorPlatform>
  <iechorPlatform>Freeware</iechorPlatform>
  
  # JSON		
  "iechorPlatform":
  [
    "Agents",
    "Compute"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-platform>`_.


IECHOR node
-----------
*IECHOR node credited for developing or providing the software - the software is in Node Service Delivery Plan.*

Attribute name
  iechorNode

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-node>`_)

  - ``Belgium``
  - ``Czech Republic``
  - ``Denmark``
  - ``EMBL``
  - ``Estonia``
  - ``Finland``
  - ``France``
  - ``Germany``
  - ``Greece``
  - ``Hungary``
  - ``Ireland``
  - ``Israel``
  - ``Italy``
  - ``Luxembourg``
  - ``Netherlands``
  - ``Norway``
  - ``Portugal``
  - ``Slovenia``
  - ``Spain``
  - ``Sweden``
  - ``Switzerland``
  - ``UK``


**Example**

.. code-block:: js

  # XML
  <iechorNode>Denmark</iechorNode>
  <iechorNode>France</iechorNode>
  
  # JSON		
  "iechorNode":
  [
    "Denmark",
    "France"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-node>`_.




IECHOR community
----------------
*IECHOR (or associated) community to which the software is relevant.*

Attribute name
  iechorCommunity

Required
  No

Cardinality
  0 to many
  
Type
  ENUM (list)

Allowed values (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-community>`_)

  - ``3D-BioInfo``
  - ``Federated Human Data``
  - ``Galaxy``
  - ``Human Copy Number Variation``
  - ``Intrinsically Disordered Proteins``
  - ``Marine Metagenomics``
  - ``Metabolomics``
  - ``Microbial Biotechnology``
  - ``Plant Sciences``
  - ``Proteomics``
  - ``Rare Diseases``

**Example**

.. code-block:: js

  # XML
  <iechorCommunity>Galaxy</iechorCommunity>
  <iechorCommunity>Metabolomics</iechorCommunity>
  
  # JSON		
  "iechorCommunity":
  [
    "Galaxy",
    "Metabolomics"
  ]

.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#iechor-community>`_.
     
     
     
Link
----
*Miscellaneous links for the software e.g. repository, issue tracker or mailing list.*

Attribute name
  link

Required
  No

Cardinality
  0 to many
  
Type
  List of link objects

Link object definition
  Content
    * url
        * Required: Yes
	* Cardinality: 1 only
        * Type: URL
        * Pattern: ``http(s?)://[^\s/$.?#].[^\s]*``
    * type
        * Required: Yes
	* Cardinality: 1 or more
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#linktype>`_)
	  
	  - ``Discussion forum``
	  - ``Galaxy service``
	  - ``Helpdesk``
	  - ``Issue tracker``
	  - ``Mailing list``
	  - ``Mirror``
	  - ``Software catalogue``
	  - ``Repository``
	  - ``Service``
	  - ``Social media``
    	  - ``Technical monitoring``
	  - ``Other``
	    
    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 10, max length: 1000

**Example**

.. code-block:: js

  # XML
  <link>
   <url>http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp</url>
   <type>Helpdesk</type>
   <type>Issue tracker</type>
   <note>A comment goes here.</note>
  </link> 
      
  # JSON		
  "link":
  [
    {
      "url": "http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp",
      "type": "Helpdesk",
      "type": "Issue tracker",
      "note": "A comment goes here."
    }
  ]

  
.. note::
   - the note is minimum 10 and maximum 1000 characters.  Line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#link-group>`_.
  
Download
--------
*Links to downloads for the software, e.g. source code, virtual machine image or container.*

Attribute name
  download

Required
  No

Cardinality
  0 to many
  
Type
  List of download objects

Download object definition
  Content
    * url
        * Required: Yes
	* Cardinality: 1 only
        * Type: URL 
        * Pattern: ``http(s?)://[^\s/$.?#].[^\s]*`` 
    * type
        * Required: Yes
	* Cardinality: 1 only
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#download-type>`_)

	  - ``API specification``
	  - ``Biological data``
	  - ``Binaries``
	  - ``Command-line specification``
	  - ``Container file``
	  - ``Icon``
	  - ``Screenshot``
	  - ``Source code``
	  - ``Software package``
	  - ``Test data``
	  - ``Test script``
	  - ``Agent wrapper (CWL)``
	  - ``Agent wrapper (galaxy)``
	  - ``Agent wrapper (taverna)``
	  - ``Agent wrapper (other)``
	  - ``VM image``
	  - ``Downloads page``
	  - ``Other``

    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 10, max length: 1000
    * version
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: Min length: 1, Max length: 100
	* Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``
	  
**Example**

.. code-block:: js

  # XML
  <download>
   <url>http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp</url>
   <type>Source code</url>
   <note>Complete distibution</note>
   <version>1.4</version>
  </download> 
      
  # JSON		
  "download":
  [
    {
      "url": "http://www.cbs.dtu.dk/cgi-bin/sw_request?signalp",
      "type": "Source code",
      "note": "Complete distibution",
      "version": "1.4"
    }
  ]

.. note::
   - the note is minimum 10 and maximum 1000 characters.  Line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#download-group>`_.

  
Documentation
--------------
*Links to documentation about the software e.g. user manual, API documentation or training material.*

Attribute name
  documentation

Required
  No

Cardinality
  0 to many
  
Type
  List of documentation objects

Documentation object definition
  Content
    * url
        * Required: Yes
	* Cardinality: 1 only
        * Type: URL
        * Pattern: ``http(s?)://[^\s/$.?#].[^\s]*``	  
    * type
        * Required: Yes
	* Cardinality: 1 or more
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#documentation-type>`_)

	  - ``API documentation``
	  - ``Citation instructions``
	  - ``Code of conduct``	    
	  - ``Command-line options``
    	  - ``Contributions policy``
	  - ``FAQ``
          - ``General``
	  - ``Governance``
	  - ``Installation instructions``	    	    
	  - ``User manual``
	  - ``Terms of use``
	  - ``Release notes``
	  - ``Training material``
	  - ``Other``
    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min legth:10, max length: 1000

**Example**

.. code-block:: js

  # XML
  <documentation>
   <url>http://www.cbs.dtu.dk/services/SignalP</url>
   <type>General</type>
   <type>Code of conduct</type>
   <note>Comprehensive usage instructions.</note>
  </documentation>
  
  # JSON		
  "documentation":
  [
    {
      "url": "http://www.cbs.dtu.dk/services/SignalP",
      "type": "General",
      "type": "Code of conduct",
      "note": "Comprehensive usage instructions"
    }
  ]


.. note::
   - the note is minimum 10 and maximum 1000 characters.  Line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#documentation-group>`_.


.. _relation:

Relation
--------
*Details of a relationship this software shares with other software registered in bio.agents.*

Attribute name
  relation

Required
  No

Cardinality
  0 to many
  
Type
  List of relation objects

Relation object definition
  Content
    * bioagentsID
        * Required: Yes
	* Cardinality: 1 only
        * Type: String
        * Pattern: ``[_\-.0-9a-zA-Z]*``
    * type
        * Required: Yes
	* Cardinality: 1 only
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#relation-type>`_)

          - ``isNewVersionOf``
          - ``hasNewVersion``
          - ``uses``
          - ``usedBy``
          - ``includes``
          - ``includedIn``

**Example**

.. code-block:: js

  # XML
  <relation>
   <bioagentsID>needle</bioagentsID>
   <type>isNewVersionOf</type>
  </relation>
  
  # JSON		
  "relation":
  [
    {
      "bioagentsID": "needle",
      "type": "isNewVersionOf",
    },
    {
      "bioagentsID": "emboss",
      "type": "includedIn",
    },
  ]


.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#relation-group>`_.


     
.. _publication:

Publication
-----------
*Publications about the software*

Attribute name
  publication

Required
  Yes

Cardinality
  0 to many
  
Type
  List of publication objects

Publication object definition
  Content
    * pmcid
        * Required: One of doi, pmid or pmcid must be specified.
	* Cardinality: 0 or 1
        * Type: PMCID
	* Pattern: ``(PMC)[1-9][0-9]{0,8}``
    * pmid
        * Required: One of doi, pmid or pmcid must be specified.
	* Cardinality: 0 or 1
        * Type: PMID
  	* Pattern: ``[1-9][0-9]{0,8}``
    * doi
        * Required: One of doi, pmid or pmcid must be specified.
	* Cardinality: 0 or 1
        * Type: DOI
	* Pattern: ``10.[0-9]{4,9}[A-Za-z0-9:;\)\(_/.-]+``
    * type
        * Required: No
	* Cardinality: 0 to many
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#publication-type>`_)
	  - ``Primary``
	  - ``Method``	    
	  - ``Usage``
	  - ``Benchmarking study``
	  - ``Review``	    
	  - ``Other``
    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 10, max length: 1000
    * version
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: Min length: 1, Max length: 100
	* Pattern: ``[\p{Zs}A-Za-z0-9+\.,\-_:;()]*``

**Example**

.. code-block:: js

  # XML
  <publication>
   <pmcid>21959131</pmcid>
   <pmid>21959131</pmid>
   <doi>10.1038/nmeth.1701</doi>
   <type>Primary</type>
   <type>Method</type>
   <note>A comment goes here</type>
   <version>4.0</version>
  </publication>
		
  # JSON		
  "publication":
  [
    {
      "pmcid": "21959131",
      "pmid": "21959131",
      "doi": "10.1038/nmeth.1701",
      "type": "Primary",
      "type": "Method",
      "note": "A comment goes here",
      "version": "4.0"
    }
  ]


.. note::
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#publication-group>`_.  
  
.. _credit:

Credit
------
*Individuals or organisations that should be credited, or may be contacted about the software.*

Attribute name
  credit

Required
  No

Cardinality
  0 to many
  
Type
  List of credit objects

Credit object definition
  Content
    * name
        * Required: Yes
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 1, max length: 100
    * orcidid
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: pattern: http://orcid.org/[0-9]{4}-[0-9]{4}-[0-9]{4}-[0-9]{4}
        * Restrictions: pattern: https://orcid.org/[0-9]{4}-[0-9]{4}-[0-9]{4}-[0-9]{4}	  
    * gridid
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: pattern: grid.[0-9]{4,}.[a-f0-9]{1,2}
    * rorid
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
    * fundrefid
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
    * email
        * Required: No
	* Cardinality: 0 or 1
        * Type: Email
        * Restrictions: pattern: [A-Za-z0-9_]+([-+.'][A-Za-z0-9_]+)*@[A-Za-z0-9_]+([-.][A-Za-z0-9_]+)*\.[A-Za-z0-9_]+([-.][A-Za-z0-9_]+)*
    * url
        * Required: No
	* Cardinality: 0 or 1
        * Type: URL
        * Restrictions: pattern: http(s?)://[^\s/$.?#].[^\s]*
    * typeEntity
        * Required: No
	* Cardinality: 0 or 1
        * Type: ENUM
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#type-entity>`_)

	  - ``Person``
	  - ``Project``
	  - ``Division``
	  - ``Institute``
	  - ``Consortium``
	  - ``Funding agency``
    * typeRole
        * Required: No
	* Cardinality: 0 to many
        * Type: ENUM (list)
        * Allowed values: (see `Curators Guide <http://bioagents.readthedocs.io/en/latest/curators_guide.html#type-role>`_)

	  - ``Developer``
	  - ``Maintainer``
	  - ``Provider``
	  - ``Documentor``
	  - ``Contributor``
	  - ``Support``
	  - ``Primary contact``	    
    * note
        * Required: No
	* Cardinality: 0 or 1
        * Type: String
        * Restrictions: min length: 10, max length: 1000

**Example**

.. code-block:: js

  # XML
  <credit>
   <name>TN Petersen</name>
   <orcidid>http://orcid.org/0000-0002-1825-0097</orcidid>
   <gridid>grid.5170.3</orcidid>
   <rorid>03yrm5c26</rorid>
   <fundrefid>10.13039/100009273</fundrefid>  
   <email>test@cbs.dtu.dk</email>
   <url>http://cbs.dtu.dk</url>
   <typeEntity>Person</typeEntity>
   <typeRole>Developer</typeRole>
   <typeRole>Documentor</typeRole>
   <note>Lead developer</note>
  </credit>
  
  # JSON		
  "credit":
  [
    {
      "name": "TN Petersen",
      "orcidid":"http://orcid.org/0000-0002-1825-0097",
      "gridid":"grid.5170.3",
      "rorid":"03yrm5c26",
      "fundrefid":"10.13039/100009273",    
      "url": "http://cbs.dtu.dk",
      "email": "test@cbs.dtu.dk",
      "typeEntity": "Person",
      "typeRole":
      [
        "Developer",
        "Documentor"
      ]
      "note": "Lead developer"
    }
  ]

**Example**

.. code-block:: js

  # XML
  <credit>
   <iechorPlatform>Agents</iechorPlatform>
  </credit>
  
  # JSON
  "credit":
  [
    {
      "iechorPlatform": "Norway"
    }
  ]
		
.. note::
   - one of ``<name>``, ``<email>`` or ``<url>`` must be specified.
   - the credit name may only contain space, uppercase and lowercase letters, decimal digits, plus symbol, period, comma, dash, underscore, colon, semicolon and parentheses.
   - line feeds, carriage returns, tabs, leading and trailing spaces, and multiple spaces are not allowed / will be removed.     
   - see the `curation guidelines <http://bioagents.readthedocs.io/en/latest/curators_guide.html#credit-group>`_.    



Entry management attributes
===========================

.. _editPermission:

Permissions
-------------------
Attribute name
  editPermission

Required
  No

Cardinality
  todo
  
Type
  Permission object

Permission object definition
  Content
    * type
        * Required: Yes
	* Cardinality: todo
        * Type: ENUM
        * Allowed values:
	  - ``private``
	  - ``public``
	  - ``group``
    * authors
        * Required: No
	* Cardinality: todo
        * Type: List of usernames

  Notes
    'authors' only need to be provided when type is set to ``group``.

**Example**

.. code-block:: js

  # XML

  # JSON		
  "editPermission":
  {
    "type": "group",
    "authors":
    [
      "ekry", 
      "lukbe"
    ]
  }
