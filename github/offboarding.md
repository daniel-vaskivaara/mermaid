
```mermaid
sequenceDiagram
    participant ServiceNow
    participant Ansible
    participant GitHub API

    ServiceNow->>Ansible: Trigger Off-boarding Playbook
    Ansible->>GitHub API: Check License Status
    GitHub API-->>Ansible: Return License Info
    Ansible->>GitHub API: Remove Copilot License
    GitHub API-->>Ansible: Confirm License Removal
    Ansible->>GitHub API: Deactivate GitHub User
    GitHub API-->>Ansible: Confirm User Deactivation
    Ansible-->>ServiceNow: Report Off-boarding Complete
```