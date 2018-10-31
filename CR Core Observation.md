## CR Core Observation

This FHIR profile sets minimum expectations for the [Observation](http://hl7.org/fhir/observation.html) resource resource to search / fetch laboratory test results associated with a patient on a clinical trial. It identifies which core elements, extensions, vocabularies and value sets SHALL be present in the resource when using this profile.


#### Example Usage Scenarios:

The following are example usage scenarios for the CR Core-Results profile:


- Query for lab results belonging to all Patients on a clinical trial

```
GET 
[base]/observations?researchstudy=12-345
```

- Query for lab results belonging to a specific Patient on a clinical trial

```
GET 
[base]/observations?researchstudy=12-345&patient:_has:ResearchSubject:identifier=12345
```

- Query for lab results belonging to a specific Patient on a clinical trial between two dates (in this example, between 6/20/2006 and 6/30/2006)

```
GET 
[base]/observations?researchstudy=17-238&patient:_has:ResearchSubject:identifier=12345&context:Encounter.date=le2006-06-30&context:Encounter.date=ge2006-06-20
```

#### Mandatory Data Elements and Terminology
The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation. Profile specific guidance and examples are provided as well. The **Formal Profile Definition** below provides the formal summary, definitions, and terminology requirements.

#### Each Observation must have:

1. a status
2. a category code of ‘laboratory’
3. a LOINC code, if available, which tells you what is being measured
4. a patient
5. a result value and, if the result value is a numeric quantity, a standard UCUM unit

#### Each Observation *should* have:

1. a time indicating when the measurement was taken
2. a reference range if available

#### Formal Profile Definition
*TBA*
