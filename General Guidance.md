## General Guidance

This section outlines important definitions and interpretations used in the CR Core IG.

### **Clinical Trial** vs. **Study** vs. **Protocol** vs. **ResearchStudy**
For the purposes of this implementation guide, the terms **clinical trial**, **study**, and **protocol** are considered equivalent. The FHIR representation of these terms **SHALL** be interpreted as ``ResearchStudy`` (*See: https://www.hl7.org/fhir/researchsubject.html*)

### De-identification of Patient data
One of the primary requirements that this implementation guide seeks to outline and provide guidance for is the de-identification of clinical trial participant data. Typically, "patient" data is captured in the ``Patient`` resource, which includes demographic and other types of information that determine who the individual is:

- https://www.hl7.org/fhir/patient.html

Within the scope of clinical research data exchange, protecting patient privacy throughout the entire process is of paramount importance. Anonymization techniques are typically used to remove identifying information from datasets before any clinical trial data is shared between parties. 

There are two FHIR resources dedicated to representing the concept of clinical research - ``ResearchSubject`` and ``ResearchStudy``. 

- https://www.hl7.org/fhir/researchsubject.html
- https://www.hl7.org/fhir/researchstudy.html


Utilizing ``ResearchSubject`` doesn't eliminate the need for ``Patient``. Instead, ``ResearchSubject`` establishes a linkage between a ``Patient`` and a particular ``ResearchStudy``, and captures the information specific to that join (e.g. subject status within the study, assigned arm, whether their consent is done, etc.)

For the purposes of this implementation guide, when sharing patient information, you'd still have a ``Patient`` resource, it simply would not contain identifying attributes such as name, etc. See the **CR Core Patient** profile for more information.

