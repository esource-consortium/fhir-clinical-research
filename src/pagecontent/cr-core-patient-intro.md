### Overview

This FHIR profile sets minimum expectations for the [Patient](http://hl7.org/fhir/patient.html) resource to search / fetch basic demographic and administrative information associated with a patient on a clinical trial. It identifies which core elements, extensions, vocabularies and value sets SHALL be present in the resource when using this profile.

FHIR servers must ensure that all patient records are associated with a protocol, represented by the linkage of a ``Patient`` and a particular ``ResearchStudy`` through the ``ResearchSubject`` resource. 

#### Mandatory Data Elements and Terminology
The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation. Profile specific guidance and examples are provided as well. The **Formal Profile Definition** below provides the formal summary, definitions, and terminology requirements.

#### Each Patient must have:

1. A patient identifier (*See Profile specific implementation guidance below*)
2. A gender

#### If data is available, each Patient shall include:
1. A non-identifying date of birth (year only)
2. A race
3. An ethnicity

#### Profile specific implementation guidance
- **MRN**s (medical record numbers) SHALL NOT be used as resource identifiers for Patients. The FHIR specification discusses this briefly. https://www.hl7.org/fhir/patient.html#ids

