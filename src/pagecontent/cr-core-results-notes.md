### Quick Start
Below is an overview of the required set of RESTful FHIR interactions - for example, search and read operations - for this profile. See the Conformance requirements for a complete list of supported RESTful interactions for this IG.

``GET [base]/Observation?ResearchStudy=[study-id]&category=laboratory``

**Example**: GET [base]/Observation?ResearchStudy=12-345&category=laboratory

*Support*: Mandatory to support search by Research Study and category code = ‘laboratory’.

*Implementation Notes*: Search based on a Research Study and laboratory category code = “laboratory”. This fetches a bundle of all Observation resources with laboratory categories for the specified ResearchStudy.

<hr>

``GET [base]/observations?ResearchStudy=[study-id]&category=laboratory&patient:_has:ResearchSubject:identifier=[subject-id]``

**Example**: GET 
[base]/observations?ResearchStudy=12-345&category=laboratory&patient:_has:ResearchSubject:identifier=12345

*Support*: Mandatory to support search by Research Subject and category code = ‘laboratory’.

*Implementation Notes*: Search based on a Research Study and Research Subject with laboratory category code = “laboratory”. This fetches a bundle of all Observation resources with laboratory categories for the specified ResearchStudy / ResearchSubject.

<hr>

``GET 
[base]/observations?ResearchStudy=[study-id]&category=laboratory&date=[date]&date=[date]``

**Example**: GET 
[base]/observations?ResearchStudy=17-238&category=laboratory&context:Encounter.date=le2006-06-30&context:Encounter.date=ge2006-06-20

*Support*: Mandatory to support search by Research Study, category code = ‘laboratory’, and date/period.

*Implementation Notes*: Search based on a Research Study and date with laboratory category code = “laboratory”. This fetches a bundle of all Observation resources with laboratory categories for the specified ResearchStudy for a specified time period.





