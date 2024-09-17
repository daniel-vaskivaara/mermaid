
```mermaid
sequenceDiagram
    participant GitHub
    participant ServiceNow
    participant GitHub Actions

    ServiceNow->>GitHub: Generate Dormant Users Report
    GitHub-->>ServiceNow: Send Report
    ServiceNow->>GitHub Actions: Schedule Workflow for Inactive Users
    GitHub Actions->>GitHub: Remove Dormant Users
    GitHub-->>GitHub Actions: Confirmation of User Removal
    GitHub Actions-->>ServiceNow: Workflow Completed
```