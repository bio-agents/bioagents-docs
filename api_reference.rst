*************
API Reference
*************


.. attention::

   - reference docs for the `bio.agents <https://bio.agents>`_ API 
   - to make suggestions about these guidelines please add comments via `GitHub <https://github.com/bio-agents/bioagentsDocs/issues/>`_
   - if you find a bug, have any questions or suggestions, please `get in touch with us <mailto:registry-support@iechor-dk.org>`_.
   - see also the `API Usage Guide <https://bioagents.readthedocs.io/en/latest/api_usage_guide.html>`_

     
The bio.agents Web API provides an easy way to access the bio.agents database.




List agents
----------
*List and search through all the available agents. Can sort, filter, and search the results.*

*HTTP GET*

.. code-block:: text

    https://bio.agents/api/agent/
    https://bio.agents/api/t/

Endpoint parameters
"""""""""""""""""""
===========    ========  =======================================  ==========  ============================================
Parameter      Required  Type                                     Default     Description        
===========    ========  =======================================  ==========  ============================================
page           No        Integer                                  1           Result page number 
format         No        String(json, api)                        json        Response media type
q              No        String                                               Query term, used for searching, 
                                                                              matches all attributes
sort           No        String(lastUpdate,                       lastUpdate  Sorts the results by choosen value
                         additionDate, name, affiliation, score)              (score only available when there is a query)
ord            No        String(desc, asc)                        desc        Orders the results by either 
                                                                              Ascending or Descending order
<attribute>    No        String                                               Filter by <attribute>. 
                                                                              List of supported attributes below.
===========    ========  =======================================  ==========  ============================================



Filtering
"""""""""
To filter the results by attribute name, the attribute name has to be added as a parameter to the URL, with the value being the desired search term, e.g. ``?name=signalp``

.. _Attributes:

Attributes
~~~~~~~~~~

These are the attributes supported by bio.agents:


==================  ============================================================================================
Parameter           Search behaviour                                                                            
==================  ============================================================================================
bioagentsID          Search for bio.agents agent ID (usually quoted - to get exact match)

                    `bioagentsID="signalp" <https://bio.agents/api/t/?bioagentsID="signalp">`_

name                Search for agent name (quoted as needed)

                    `name=signalp <https://bio.agents/api/t/?name=signalp>`_ 
homepage            Exact search for agent homepage URL (**must** be quoted)

                    `homepage="http://cbs.dtu.dk/services/SignalP/" <https://bio.agents/api/t/?homepage="http://cbs.dtu.dk/services/SignalP/">`_ 
description         Search over agent description (quoted as needed)

                    `description="peptide cleavage" <https://bio.agents/api/t/?description="peptide%20cleavage">`_ 
version             Exact search for agent version (**must** be quoted)

                    `version="4.1" <https://bio.agents/api/t/?version="4.1">`_ 
topic               Search for EDAM Topic (term) (quoted as needed)

                    `topic="Proteomics" <https://bio.agents/api/t/?topic="Proteomics">`_ 

topicID             Exact search for EDAM Topic (URI): **must** be quoted                                               

                    `topicID="topic_3510" <https://bio.agents/api/t/?topicID="topic_3510">`_ 
function            Fuzzy search over function (input, operation, output, note and command)                         

                    `function="Sequence analysis" <https://bio.agents/api/t/?function="Sequence%20analysis">`_ 
operation           Fuzzy search for EDAM Operation (term) (quoted as needed)                              

                    `operation="Sequence analysis" <https://bio.agents/api/t/?operation="Sequence%20analysis">`_ 
operationID         Exact search for EDAM Operation (ID) (**must** be quoted)

                    `operationID="operation_2403" <https://bio.agents/api/t/?operationID="operation_2403">`_ 
dataType            Fuzzy search over input and output for EDAM Data (term) (quoted as needed)                              

                    `dataType="Protein sequence" <https://bio.agents/api/t/?dataType="Protein%20sequence">`_ 
dataTypeID          Exact search over input and output for EDAM Data (ID) (**must** be quoted)                           

                    `dataTypeID="data_2976" <https://bio.agents/api/t/?dataTypeID="data_2976">`_ 
dataFormat          Fuzzy search over input and output for EDAM Format (term) (quoted as needed)                      

                    `dataFormat="FASTA" <https://bio.agents/api/t/?dataFormat="FASTA">`_ 
dataFormatID        Exact search over input and output for EDAM Format (ID) (**must** be quoted)

                    `dataFormatID="format_1929" <https://bio.agents/api/t/?dataFormatID="format_1929">`_ 
input               Fuzzy search over input for EDAM Data and Format (term) (quoted as needed)

                    `input="Protein sequence" <https://bio.agents/api/t/?input="Protein%20sequence">`_ 
inputID             Exact search over input for EDAM Data and Format (ID) (**must** be quoted)                                         

                    `inputID="data_2976" <https://bio.agents/api/t/?inputID="data_2976">`_ 
inputDataType       Fuzzy search over input for EDAM Data (term) (quoted as needed)     

                    `inputDataType="Protein sequence" <https://bio.agents/api/t/?inputDataType="Protein%20sequence">`_ 
inputDataTypeID     Exact search over input for EDAM Data (ID) (**must** be quoted)

                    `inputDataTypeID="data_2976" <https://bio.agents/api/t/?inputDataTypeID="data_2976">`_ 
inputDataFormat     Fuzzy search over input for EDAM Format (term) (quoted as needed)                                 

                    `inputDataFormat="FASTA" <https://bio.agents/api/t/?inputDataFormat="FASTA">`_ 
inputDataFormatID   Exact search over input for EDAM Format (ID) (**must** be quoted)

                    `inputDataFormatID="format_1929" <https://bio.agents/api/t/?inputDataFormatID="format_1929">`_ 
output              Fuzzy search over output for EDAM Data and Format (term) (quoted as needed)

                    `output="Sequence alignment" <https://bio.agents/api/t/?output="Sequence%20alignment">`_ 
outputID            Exact search over output for EDAM Data and Format (ID) (**must** be quoted)

                    `outputID="data_0863" <https://bio.agents/api/t/?outputID="data_0863">`_ 
outputDataType      Fuzzy search over output for EDAM Data (term) (quoted as needed)

                    `outputDataType="Sequence alignment" <https://bio.agents/api/t/?outputDataType="Sequence%20alignment">`_ 
outputDataTypeID    Exact search over output for EDAM Data (ID) (**must** be quoted)

                    `outputDataTypeID="data_0863" <https://bio.agents/api/t/?outputDataTypeID="data_0863">`_ 
outputDataFormat    Fuzzy search over output for EDAM Format (term) (quoted as needed)                                

                    `outputDataFormat="ClustalW format" <https://bio.agents/api/t/?outputDataFormat="ClustalW%20format">`_ 
outputDataFormatID  Exact search over output for EDAM Format (ID) (**must** be quoted)

                    `outputDataFormatID="format_1982" <https://bio.agents/api/t/?outputDataFormatID="format_1982">`_ 
agentType            Exact search for agent type

                    `agentType="Command-line agent" <https://bio.agents/api/t/?agentType="Command-line%20agent">`_ 
collectionID        Exact search for agent collection (normally quoted)

                    `collectionID="Rare Disease" <https://bio.agents/api/t/?collectionID="Rare%20Disease">`_ 
maturity            Exact search for agent maturity

                    `maturity=Mature <https://bio.agents/api/t/?maturity=Mature>`_ 
operatingSystem     Exact search for agent operating system                                                          

                    `operatingSystem=Linux <https://bio.agents/api/t/?operatingSystem=Linux>`_ 
language            Exact search for programming language

                    `language=Java <https://bio.agents/api/t/?language=Java>`_ 
cost                Exact search for cost 

                    `cost="Free of charge" <https://bio.agents/api/t/?cost="Free%20of%20charge">`_ 
license             Exact search for software or data usage license (quoted as needed)

                    `license="GPL-3.0" <https://bio.agents/api/t/?license="GPL-3.0">`_ 
accessibility       Exact search for agent accessibility                                      

                    `accessibility="Open access" <https://bio.agents/api/t/?accessibility="Open%20access">`_ 
credit              Fuzzy search over credit (name, email, URL, ORCID iD, type of entity, type of role and note)    

                    `credit="Henrik Nielsen" <https://bio.agents/api/t/?credit="Henrik%20Nielsen">`_ 
creditName          Exact search for name of credited entity                                                        

                    `creditName="Henrik Nielsen" <https://bio.agents/api/t/?creditName="Henrik%20Nielsen">`_ 
creditTypeRole      Exact search for role of credited entity 

                    `creditTypeRole=Developer <https://bio.agents/api/t/?creditTypeRole=Developer>`_ 
creditTypeEntity    Exact search for type of credited entity 

                    `creditTypeEntity="Funding agency" <https://bio.agents/api/t/?creditTypeEntity="Funding%20agency">`_ 
creditOrcidID       Exact search for ORCID iD of credited entity (**must** be quoted)

                    `creditOrcidID="0000-0001-5121-2036" <https://bio.agents/api/t/?creditOrcidID="0000-0001-5121-2036">`_ 
publication         Fuzzy search over publication (DOI, PMID, PMCID, publication type and agent version) (quoted as needed)            

                    `publication=10.12688/f1000research.12974.1 <https://bio.agents/api/t/?publication=10.12688/f1000research.12974.1>`_ 
publicationID       Exact search for publication ID (DOI, PMID or PMCID) (**must** be quoted)

                    `publicationID="10.12688/f1000research.12974.1" <https://bio.agents/api/t/?publicationID="10.12688/f1000research.12974.1">`_ 
publicationType     Exact search for publication type

                    `publicationType=Primary <https://bio.agents/api/t/?publicationType=Primary>`_ 
publicationVersion  Exact search for agent version associated with a publication (**must** be quoted)

                    `publicationVersion="1.0" <https://bio.agents/api/t/?publicationVersion="1.0">`_ 
link                Fuzzy search over general link (URL, type and note) (quote as needed)

                    `link="Issue tracker" <https://bio.agents/api/t/?link="Issue%20tracker">`_ 
linkType            Exact search for type of information found at a link

                    `linkType="Issue tracker" <https://bio.agents/api/t/?linkType="Issue tracker">`_
documentation       Fuzzy search over documentation link (URL, type and note) (quote as needed)                          

                    `documentation=Manual <https://bio.agents/api/t/?documentation="User manual">`_ 
documentationType   Exact search for type of documentation

                    `documentationType=Manual <https://bio.agents/api/t/?documentationType="User manual">`_ 
download            Fuzzy search over download link (URL, type, version and note) (quote as needed)

                    `download=Binaries <https://bio.agents/api/t/?download=Binaries>`_ 
downloadType        Exact search for type of download

                    `downloadType=Binaries <https://bio.agents/api/t/?downloadType=Binaries>`_ 
downloadVersion     Exact search for agent version associated with a download (**must** be quoted)

                    `downloadVersion="1.0" <https://bio.agents/api/t/?downloadVersion="1.0">`_ 
otherID             Fuzzy search over alternate agent IDs (ID value, type of ID and version)                         

                    `otherID="rrid:SCR_015644" <https://bio.agents/api/t/?otherID="rrid:SCR_015644">`_ 

otherIDValue        Exact search for value of alternate agent ID (**must** be quoted)

                    `otherIDValue="rrid:SCR_015644" <https://bio.agents/api/t/?otherIDValue="rrid:SCR_015644">`_		    
otherIDType         Exact search for type of alternate agent ID                                

                    `otherIDType=RRID <https://bio.agents/api/t/?otherIDType=RRID>`_ 
otherIDVersion      Exact search for agent version associated with an alternate ID (**must** be quoted)

                    `otherIDVersion="1.0" <https://bio.agents/api/t/?otherIDVersion="1.0">`_ 
==================  ============================================================================================


.. important::
   Values of the following parameters **must** be given in quotes to get sensible (or any) results:
     * ``homepage``
     * ``version``
     * ``topicID``
     * ``operationID``
     * ``dataTypeID``       
     * ``dataFormatID``
     * ``inputID``
     * ``inputDataTypeID``
     * ``inputDataFormatID``
     * ``outputID``
     * ``outputDataTypeID``
     * ``outputDataFormatID``
     * ``creditOrcidID``            
     * ``publicationID``
     * ``publicationVersion``
     * ``downloadVersion``
     * ``otherIDValue``
     * ``otherIDVersion``       

    *e.g.* 
     * https://bio.agents/api/agent?topicID="topic_3510"
       
   Values of other parameters can be quoted or unquoted:
     *  Unquoted values invoke a fuzzy word search: it will search for fuzzy matches of words in the search phrase, to the target field
     *  Quoted values invoke an exact phrase search; it will search for an exact match of the full-length of the search phrase, to the target field (matches to target substrings are allowed)

   *e.g.*
     * https://bio.agents/api/agent?bioagentsID="blast" returns the agent with bioagentsID of "blast" (the "canonical" blast)
     * https://bio.agents/api/agent?bioagentsID=blast returns all agents with "blast" in their bioagentsID (all blast flavours)

	
.. caution::
   The parameters are (currently) case-sensitive, *e.g.* you **must** use ``&bioagentsID=`` and not ``&bioagentsid``


.. important=  The API parameters will be made case-insensitive in future.


Example
"""""""

.. code-block:: bash

   curl -X GET "https://bio.agents/api/agent/?page=1&format=json&name=signalp&sort=name&ord=asc&q=protein-signal-peptide-detection"

.. note::
   An EDAM concept ID can be specified as a concept URI or ID:
     * Concept URI *e.g.* ``http://edamontology.org/operation_2403``
     * Concept ID *e.g.* ``operation_2403``

   In future we may add support for:  
     * Concept CURIE *e.g.* ``EDAM:operation_2403``
     * Numerical ID *e.g.* ``2403``

   Note: URIs and IDs **must** be quoted, *e.g.* ``&topicID="operation_2403"``
   
     

Response data
"""""""""""""
================== ========================================================================== =========================
Key Name           Description                                                                Example
================== ========================================================================== =========================
count              The total agent count results for your query                                2313
previous           Link to the previous page                                                  ?page=4
next               Link to the next page                                                      ?page=6
list               An array with multiple agents                                               ARRAY
                   and their relative information 
================== ========================================================================== =========================


Agent detail
-----------
*Obtain information about a single agent.*

*HTTP GET*

.. code-block:: text

    https://bio.agents/api/agent/:id/
    https://bio.agents/api/t/:id/
    https://bio.agents/api/:id/


Endpoint Parameters
"""""""""""""""""""
=========  ========  ======================  =======  ===================
Parameter  Required  Type                    Default  Description        
=========  ========  ======================  =======  ===================
id         Yes       String                           bioagentsID 
format     No        String(json, xml, api)  json     Response media type
=========  ========  ======================  =======  ===================


Example
"""""""

.. code-block:: bash

   curl -X GET "https://bio.agents/api/agent/signalp/?format=json"


.. caution::

   bio.agents supports upload/download of data in XML format compliant to `bioagentsScheme v3.0.0 <https://github.com/bio-agents/bioagentsSchema>`_.  If you want to download in XML format you should use these endpoints (see `Agent detail <https://bioagents.readthedocs.io/en/latest/api_reference.html#agent-detail>`_ below):

   .. code-block:: text

    https://bio.agents/api/agent/id/
    https://bio.agents/api/t/id/
    https://bio.agents/api/id/

   *e.g.* https://bio.agents/api/agent/signalp

   Were you to try to get XML format returned from a *search* over bio.agents

   *e.g.* https://bio.agents/api/agent?agentid=signalp&format=xml

   currently you'd get garbled / invalid XML (don't use it!) - we're looking at a fix.

    
   

Register a agent
---------------

*Register a new agent.*


.. important:: This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/agent/
    https://bio.agents/api/t/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ======== ====================================================================================================================================
Parameter  Required  Type     Description        
=========  ========  ======== ====================================================================================================================================
data       Yes       Agent     Agent you wish to register.
                              See an `example agent <https://bio.agents/api/agent/SignalP?format=json>`_.
=========  ========  ======== ====================================================================================================================================

.. note:: It is possible to specify editing permissions for agents. Learn how to manage :ref:`Editing_permissions`.

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   Media type
                         application/xml)   
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   -d '<resource>' "https://bio.agents/api/agent/"


Validate registering a agent
---------------------------

*Test registering a agent without it actually being saved into the database.*

.. important::
   This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/agent/validate/
    https://bio.agents/api/t/validate/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ======== ====================================================================================================================================
Parameter  Required  Type     Description        
=========  ========  ======== ====================================================================================================================================
data       Yes       Agent     Agent you wish to validate.
                              See an `example agent <https://bio.agents/api/agent/SignalP?format=json>`_.
=========  ========  ======== ====================================================================================================================================


Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   Media type
                         application/xml)   
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   -d '<resource>' "https://bio.agents/api/agent/validate/"


Update a agent
-------------
*Update a agent description.*

.. important:: This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP PUT*

.. code-block:: text

    https://bio.agents/api/agent/:id/
    https://bio.agents/api/t/:id/
    https://bio.agents/api/:id/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ======== ====================================================================================================================================
Parameter  Required  Type     Description        
=========  ========  ======== ====================================================================================================================================
id         Yes       String   bioagentsID 
data       Yes       Agent     Description with which you wish to update the agent
                              See an `example agent <https://bio.agents/api/agent/SignalP?format=json>`_.
=========  ========  ======== ====================================================================================================================================

.. note:: It is possible to specify editing permissions for agents. Learn how to manage :ref:`Editing_permissions`.

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   Media type
                         application/xml)   
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X PUT -H "Content-Type: application/json" \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   -d '<resource>' "https://bio.agents/api/agent/SignalP"



Validate updating a agent
------------------------
*Test updating a agent without it actually being saved into the database.*

.. important::
   This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP PUT*

.. code-block:: text

    https://bio.agents/api/agent/:id/validate/
    https://bio.agents/api/t/:id/validate/
    https://bio.agents/api/:id/validate/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ======== ====================================================================================================================================
Parameter  Required  Type     Description        
=========  ========  ======== ====================================================================================================================================
id         Yes       String   bioagentsID 
data       Yes                Agent Description with which you wish to update the agent for validation
                              See an `example agent <https://bio.agents/api/agent/SignalP?format=json>`_.
=========  ========  ======== ====================================================================================================================================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   Media type
                         application/xml)   
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X PUT -H "Content-Type: application/json" \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   -d '<resource>' "https://bio.agents/api/agent/SignalP/validate/"


.. _Editing_permissions:

Editing permissions
-------------------
*Manage editing permissions for the registered agents.*

There are currently three types of editing permissions supported by the system:

.. _Private:

Private
"""""""
A private agent can only be edited by the creator of the agent. This is the default option. In order to set this kind of permission, add the following info into the agent data:

.. code-block:: text

    "editPermission": {
        "type": "private"
    }

.. _Public:

Public
""""""
Public agent can be modified by any user registered in the system. In order to set this kind of permission, add the following info into the agent data:

.. code-block:: text

    "editPermission": {
        "type": "public"
    }

.. _Group:

Group
"""""
Specify a list of users in the system that can edit the agent. In order to set this kind of permission, add the following info into the agent data:

.. code-block:: text

    "editPermission": {
        "type": "private",
        "authors": [
            "registered_user_1", "registered_user_2"
        ]
    }


Delete a agent
-------------

*Removes a agent from the registry.*

.. important::
   This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP DELETE*

.. code-block:: text

    https://bio.agents/api/agent/:id/
    https://bio.agents/api/t/:id/
    https://bio.agents/api/:id/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ======== ====================================================================================================================================
Parameter  Required  Type     Description        
=========  ========  ======== ====================================================================================================================================
id         Yes       String   bioagentsID
=========  ========  ======== ====================================================================================================================================


Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X DELETE \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   "https://bio.agents/api/agent/SignalP"


List used terms
---------------
*Obtain a list of terms registered with agents for some attributes, e.g. a list of names of all agents.*

*HTTP GET*

.. code-block:: text

    https://bio.agents/api/used-terms/:attribute

Endpoint Parameters
"""""""""""""""""""
=========  ========  ==============================================================  =======  ==========================================================
Parameter  Required  Type                                                            Default  Description        
=========  ========  ==============================================================  =======  ==========================================================
attribute  Yes       String(name, topic, functionName, input, output, credits, all)           Attribute for which a list of used terms will be returned
format     No        String(json, xml, api)                                          json     Response media type
=========  ========  ==============================================================  =======  ==========================================================


Example
"""""""

.. code-block:: bash

   curl -X GET "https://bio.agents/api/used-terms/name/?format=json"

Response data
"""""""""""""
================== ====================
Key Name           Description         
================== ====================
data               A list of used terms
================== ====================


Create a user account
---------------------

*Creates a user account and emails a verification email.*

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/registration/

POST data
"""""""""
==================  ========  ======  ========================================================================== =========================
Key Name            Required  Type    Description                                                                Example
==================  ========  ======  ========================================================================== =========================
username            Yes       String  Account username                                                           username
password1           Yes       String  Password                                                                   password
password2           Yes       String  Repeated password                                                          password
email               Yes       String  Account email. The verification email will be sent to this address         example@example.org
==================  ========  ======  ========================================================================== =========================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   POST data media type
                         application/xml)   
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -d '{"username":"username", "password1":"password", \
   "password2":"password", "email":"example@example.org"}' \
   "https://bio.agents/api/rest-auth/registration/"



Verify a user account
---------------------

*Verifies a user account based on the emailed verification key.*

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/registration/verify-email/

POST data
"""""""""
==================  ========  ======  ========================================================================== ================================================================
Key Name            Required  Type    Description                                                                Example
==================  ========  ======  ========================================================================== ================================================================
key                 Yes       String  Verification key from account creation email                               ndwowtbpmlk5zxdxfrwgu2822xynjidhizhwosycve7hro1of156hjwdsf1f6gbn
==================  ========  ======  ========================================================================== ================================================================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   POST data media type
                         application/xml)   
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -d '{"key":"ndwowtbpmlk5zxdxfrwgu2822xynjidhizhwosycve7hro1of156hjwdsf1f6gbn"}' \
   "https://bio.agents/api/rest-auth/registration/verify-email/"


.. _Token:

Log in / obtain token
---------------------

*Logs the user in and returns an authentication token.*

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/login/

POST data
"""""""""
==================  ========  ======  ========================================================================== =========================
Key Name            Required  Type    Description                                                                Example
==================  ========  ======  ========================================================================== =========================
username            Yes       String  Account username                                                           username
password            Yes       String  Password                                                                   password
==================  ========  ======  ========================================================================== =========================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   POST data media type
                         application/xml)   
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -d '{"username":"username","password":"password"}' \
   "https://bio.agents/api/rest-auth/login/"

Response data
"""""""""""""
================== ====================
Key Name           Description         
================== ====================
key                Authentication token
================== ====================

Get user information
--------------------
*Return information about the logged in user account, including a list of registered agent (name, id, version, additionDate, lastUpdate)*

.. important::
   This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP GET*

.. code-block:: text

    https://bio.agents/api/rest-auth/user/

Endpoint Parameters
"""""""""""""""""""
=========  ========  ==============================================================  =======  ==========================================================
Parameter  Required  Type                                                            Default  Description        
=========  ========  ==============================================================  =======  ==========================================================
format     No        String(json, xml, api)                                          json     Response media type
=========  ========  ==============================================================  =======  ==========================================================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X GET \
   -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
   "https://bio.agents/api/rest-auth/user/?format=json"

Response data
"""""""""""""
================== ========================================================
Key Name           Description         
================== ========================================================
username           Account username
email              Account email
resources          List of registered agents 
                   (limited to name, id, version, additionDate, lastUpdate)
================== ========================================================


Log out
-------
*Log out of the system.*

.. important::
   This method requires the user to be authenticated. Learn how to :ref:`Token`.

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/logout/

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Authorization  Yes       String('Token <authorization token>')      Authorization header.
                                                                    Learn how to :ref:`Token`.
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

  curl -X POST 
  -H "Authorization: Token 028595d682541e7e1a5dcf2306eccb720dadafd7" \
  "https://bio.agents/api/rest-auth/logout/"


Reset user password
-------------------

*Send a password reset email.*

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/password/reset/

POST data
"""""""""
==================  ========  ======  ========================================================================== =========================
Key Name            Required  Type    Description                                                                Example
==================  ========  ======  ========================================================================== =========================
email               Yes       String  Account email                                                              example@example.org
==================  ========  ======  ========================================================================== =========================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   POST data media type
                         application/xml)   
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -d '{"email":"example@example.org"}' \
   "https://bio.agents/api/rest-auth/password/reset/"

Confirm password reset
----------------------

*Confirm a password reset using uid and token from a password reset email.*

*HTTP POST*

.. code-block:: text

    https://bio.agents/api/rest-auth/password/reset/confirm/

POST data
"""""""""
==================  ========  ======  ========================================================================== =========================
Key Name            Required  Type    Description                                                                Example
==================  ========  ======  ========================================================================== =========================
uid                 Yes       String  UID from password reset email                                              MQ
token               Yes       String  Token from password reset email                                            4ct-67e90a1ab4f22fbb9b9f
password1           Yes       String  New password                                                               new_password
password2           Yes       String  New password repeated                                                      new_password
==================  ========  ======  ========================================================================== =========================

Headers
"""""""
=============  ========  =========================================  ==============================================================================================
Parameter      Required  Allowed values                             Description        
=============  ========  =========================================  ==============================================================================================
Content-Type   Yes       String(application/json,                   POST data media type
                         application/xml)   
=============  ========  =========================================  ==============================================================================================

Example
"""""""

.. code-block:: bash

   curl -X POST -H "Content-Type: application/json" \
   -d '{"uid":"MQ", "token":"4ct-67e90a1ab4f22fbb9b9f", \
   "password1":"new_password", "password2":"new_password"}' \
   "https://bio.agents/api/rest-auth/password/reset/confirm/"

Stats
-----
*Compile stats about a the registry.*

*HTTP GET*

.. code-block:: text

    https://bio.agents/api/stats

Example
"""""""

.. code-block:: bash

   curl -X GET "https://bio.agents/api/stats"
