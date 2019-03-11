.. _descGenPer:

Descripción de los metadatos 
============================

Las propiedades del perfil de aplicación para pautas de repositorios de literatura de OpenAire son listadas en esta sección. Los niveles de requerimientos siguientes para las propiedades de metadata usadas son:

Obligatorio (M)
  La propiedad siempre debe estar presente en los metadatos. No se permite un valor vacío para la propiedad.

Obligatorio si es aplicable (MA)
  Cuando se puede obtener el valor de la propiedad, debe estar presente en los metadatos.

Recomendado (R)
  Se recomienda el uso de la propiedad.

Opcional (O)
  No es importante si la propiedad se usa o no, pero si se usa puede proporcionar información complementaria sobre el recurso.

Esta documentación utiliza las siguientes abreviaturas de espacio de nombres:

* ``dc``: http://purl.org/dc/elements/1.1/
* ``dcterms``: http://purl.org/dc/terms/
* ``datacite``: http://datacite.org/schema/kernel-4
* ``oaire``: http://namespace.openaire.eu/schema/oaire/


======================================== ============================= ========================================================================================
Campo-OpenAIRE                           Elemento Metadata              Refinamiento por vocabulario
======================================== ============================= ========================================================================================
:ref:`dci:title`                         datacite:title                :ref:`title type <vocab:titletype_titletype>`
:ref:`dci:creator`                       datacite:creator              :ref:`name type <vocab:nametype_nametype>`
:ref:`dci:contributor`                   datacite:contributor          | :ref:`name type <vocab:nametype_nametype>`
                                                                       | :ref:`tipo contribuidor <vocab:contributortype_contributortype>`
:ref:`dc:contributor.rol`                dc:contributorRol              
:ref:`aire:fundingReference`             oaire:fundingReference        :ref:`funderIdentifier type <vocab:funderIdentifiertype_identifiertype>`
:ref:`dci:alternativeIdentifier`         datacite:alternateIdentifier  :ref:`alternateIdentifier type <vocab:alternateIdentifiertype_identifiertype>`
:ref:`dci:relatedIdentifier`             datacite:relatedIdentifier    | :ref:`relatedIdentifier type <vocab:relatedIdentifiertype_identifiertype>`
                                                                       | :ref:`relation type <vocab:relationtype_relationtype>`
                                                                       | :ref:`resourcetype general <vocab:resourcetypegeneral_resourcetypegeneral>`
:ref:`dci:dateEmbargo`                   datacite:date                 :ref:`date type <vocab:datetype_datetype>`
:ref:`dc:language`                       dc:language                   `IETF BCP 47`_, `ISO 639-3`_
:ref:`dc:publisher`                      dc:publisher
:ref:`dci:datePublication`               datacite:date                 :ref:`date type <vocab:datetype_datetype>`
:ref:`aire:resourceType`                 oaire:resourceType            `COAR Resource Type Vocabulary`_
:ref:`dc:description`                    dc:description
:ref:`dc:format`                         dc:format
:ref:`dci:identifier`                    datacite:identifier           :ref:`identifier type <vocab:identifiertype_identifiertype>`
:ref:`dci:accessrights`                  datacite:rights               `COAR Access Right Vocabulary`_
:ref:`dc:source`                         dc:source
:ref:`dci:subject`                       datacite:subject              
:ref:`aire:licenseCondition`             oaire:licenseCondition
:ref:`dc:coverage`                       dc:coverage
:ref:`dci:size`                          datacite:size
:ref:`dci:geolocation`                   datacite:geoLocation
:ref:`aire:version`                      oaire:version                 `COAR Version Vocabulary`_ 
:ref:`aire:file`                         oaire:file                    `COAR Access Right Vocabulary`_
:ref:`aire:citationTitle`                oaire:citationTitle 	
:ref:`aire:citationVolume`               oaire:citationVolume
:ref:`aire:citationIssue`                oaire:citationIssue
:ref:`aire:citationStartPage`            oaire:citationStartPage
:ref:`aire:citationEndPage`              oaire:citationEndPage
:ref:`aire:citationEdition`              oaire:citationEdition
:ref:`aire:citationConferencePlace`      oaire:citationConferencePlace
:ref:`aire:citationConferenceDate`       oaire:citationConferenceDate
:ref:`dct:audience`                      dcterms:audience
======================================== ============================= ========================================================================================


El perfil de aplicación es implementado en el esquema XML.
`Los archivos <https://github.com/openaire/guidelines-literature-repositories/tree/master/schemas>`_ 
para el perfil de aplicación y `archivos XML de ejemplo <https://github.com/openaire/guidelines-literature-repositories/tree/master/samples>`_ son parte de estas Directrices o pautas y también están disponibles en el `repositorio de GitHub <https://github.com/openaire/guidelines-literature-repositories>`_.

En los documentos de metadatos de XML, el esquema se debe declarar de la siguiente manera:

.. code-block:: xml
   :linenos:

   <resource xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
     xmlns:dc="http://purl.org/dc/elements/1.1/"
     xmlns:dcterms="http://purl.org/dc/terms/"
     xmlns:datacite="http://datacite.org/schema/kernel-4"
     xmlns="http://namespace.openaire.eu/schema/oaire/"
     xsi:schemaLocation="http://namespace.openaire.eu/schema/oaire/ https://www.openaire.eu/schema/repo-lit/4.0/openaire.xsd">

.. _COAR Resource Type Vocabulary: http://vocabularies.coar-repositories.org/documentation/resource_types/
.. _COAR Access Right Vocabulary: http://vocabularies.coar-repositories.org/documentation/access_rights/
.. _COAR Version Vocabulary: http://vocabularies.coar-repositories.org/documentation/version_types/
.. _IETF BCP 47: http://tools.ietf.org/rfc/bcp/bcp47.txt
.. _ISO 639-3: https://iso639-3.sil.org/ 

.. toctree::
   :numbered:
   :maxdepth: 1
   :hidden:

   field_title
   field_creator
   field_contributor
   field_contributorRol
   field_projectid
   field_alternativeidentifier
   field_relatedidentifier
   field_embargoenddate
   field_language
   field_publisher
   field_publicationdate
   field_publicationtype
   field_description
   field_format
   field_resourceidentifier
   field_accessrights
   field_source
   field_subject
   field_licensecondition
   field_coverage
   field_size
   field_geolocation
   field_resourceversion
   field_filelocation
   field_citationtitle
   field_citationvolume
   field_citationissue
   field_citationstartpage
   field_citationendpage
   field_citationedition
   field_citationconferenceplace
   field_citationconferencedate
   field_audience