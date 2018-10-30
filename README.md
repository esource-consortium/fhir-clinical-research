# eSource Consortium FHIR for Local Labs
## Overview

This implementation guide is based on FHIR Version 3.0.1 and defines the minimum conformance requirements necessary for exchanging clinical trial laboratory result data. Typically, this exchange will be between a clinical trial site and a clinical trial sponsor.

The FHIR profiles referenced in this guide are closely aligned with the profiles as defined in [US Core](http://www.hl7.org/fhir/us/core/). 

The main distinguishing factor of the profiles contained in this guide is the emphasis on de-identification of patient data, and the usage/adoption of the "Research" FHIR Resources ``ResourceSubject`` and ``ResearchStudy``. 


## Use Cases
This implementation guide describes several use cases and sets search expectations for each.

1. A research study sponsor requests laboratory data for a research study

Additional use cases TBA.