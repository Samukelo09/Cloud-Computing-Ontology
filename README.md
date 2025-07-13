# Cloud Computing Ontology

This ontology standardizes the **description**, **classification**, and **management** of cloud resources, services, providers, and metrics across various cloud computing platforms.

## Description

The ontology provides formal semantics for concepts such as:

- Cloud computing models (IaaS, PaaS, SaaS)
- Cloud resources (Compute, Network, Storage)
- Cloud service providers (e.g., AWS, Azure, Google Cloud)
- Availability & compliance features (e.g., Auto Scaling, Regulatory Compliance)
- Cost and performance metrics (e.g., SLA, CPU count, bandwidth, latency)

Built in **OWL 2 DL**, this ontology is designed to support:
-  Interoperability
-  Service discovery
-  Automated reasoning
-  Resource optimization

##  Key Classes & Properties

### Classes
- `Cloud_Service_Provider`
- `Cloud_Resource`
- `Compute_Resource`, `Storage_Resource`, `Network_Resource`
- `Cloud_Service`, `Virtual_Machine_Service`, `Serverless_Compute_Service`
- `Performance_Metric`, `Availability_Feature`, `Cost_Model`, `Compliance_Feature`

### Object Properties
- `hasServiceModel`
- `isProvidedBy`
- `hasAvailabilityFeature`
- `hasComplianceFeature`
- `hasCostModel`
- `hasPerformanceMetric`

### Data Properties
- `hasMemory`
- `hasCPUCount`
- `hasBandwidth`
- `hasLatency`
- `hasPrice`

##  SPARQL Query Example

```sparql
PREFIX : <http://www.semanticweb.org/student/ontologies/2025/2/CloudComputingOntology#>

SELECT ?service
WHERE {
  ?service :hasComplianceFeature :Regulatory_Compliance .
}
