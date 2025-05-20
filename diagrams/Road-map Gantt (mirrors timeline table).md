```mermaid
gantt
    dateFormat  YYYY-MM
    title FHIR-ORKR Development Road-map
    section Stage 1
    Profiles & IG           :active, p1, 2025-06, 3m
    Validation Pipeline     :p2, after p1, 3m
    section Stage 2
    Containerisation        :p3, 2025-10, 3m
    Security & GraphQL      :p4, after p3, 3m
    Knowledge Layer         :p5, after p4, 3m
    CoreTrustSeal Audit     :p6, after p5, 1m
    section Stage 3
    Cloud Deployments       :p7, 2026-04, 3m
    Pilot Analyses          :p8, after p7, 2m
    Stretch CKD Pipeline    :p9, after p8, 1m
    v1.0 Release            :milestone, rel, 2026-06, 0d
```
