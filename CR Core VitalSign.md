## CR Core Observation

This FHIR profile sets minimum expectations for the [Observation](http://hl7.org/fhir/observation.html) resource resource to search / fetch vital sign measurements associated with a patient on a clinical trial. It identifies which core elements, extensions, vocabularies and value sets SHALL be present in the resource when using this profile.

FHIR servers must ensure that all vital sign measurements are associated with a protocol. Non protocol specific vital signs SHOULD NOT be returned.

#### Example Usage Scenarios:

The following are example usage scenarios for the CR Core-VitalSign profile:


- Query for vital signs belonging to all Patients on a clinical trial

**Request**
```
GET 
[base]/observations?researchstudy=12-345&category=vital-signs
```

**Response**


<hr>



- Query for vital signs belonging to a specific Patient on a clinical trial

```
GET 
[base]/observations?researchstudy=12-345&category=vital-signs&patient:_has:ResearchSubject:identifier=12345
```

- Query for vital signs belonging to a specific Patient on a clinical trial between two dates (in this example, between 6/20/2006 and 6/30/2006)

```
GET 
[base]/observations?researchstudy=17-238&category=vital-signs&patient:_has:ResearchSubject:identifier=12345&context:Encounter.date=le2006-06-30&context:Encounter.date=ge2006-06-20
```

#### Mandatory Data Elements and Terminology
The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation. Profile specific guidance and examples are provided as well. The **Formal Profile Definition** below provides the formal summary, definitions, and terminology requirements.

#### Each Observation must have:

1. a status
2. a category code of ‘vital-signs’
3. a LOINC code, if available, which tells you what is being measured
4. a patient
5. a result value and, if the result value is a numeric quantity, a standard UCUM unit

#### Formal Profile Definition
*TBA*
