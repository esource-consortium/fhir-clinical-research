## General Security Considerations

CR Core transactions often make use of clinical trial participant-specific information which could be exploited by malicious actors, resulting in exposure of protected health information (PHI). For this reason, transactions must be secured appropriately with access to limited authorized individuals, data protected in transit, and appropriate audit measures taken.

Implementers should be aware of the security considerations associated with FHIR transactions, particularly those related to:

- [Communication](http://hl7.org/fhir/security.html#http)
- [Authentication](http://hl7.org/fhir/security.html#authentication)
- [Authorization/Access Control](http://hl7.org/fhir/security.html#authorization/access%20control)
- [Audit Logging](http://hl7.org/fhir/security.html#audit)
- [Digital Signatures](http://hl7.org/fhir/security.html#digital%20signatures)
- [Security Labels](http://hl7.org/fhir/security-labels.html)
- [Narrative](http://hl7.org/fhir/security.html#narrative)

For the purposes of CR Core, security conformance requirements are as follows:
- Systems SHALL establish a risk analysis and management regime that conforms with HIPAA security regulatory requirements.
- Systems SHALL use TLS version 1.2 or higher for all transmissions not taking place over a secure network connection.
- *Additional requirements TBA*

