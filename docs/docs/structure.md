# Struktur Repo Ansible

Ini adalah diagram visual dari struktur repo Ansible + AWX yang direkomendasikan.  

```mermaid
graph TD
    A[ansible/] --> B[ansible.cfg]

    A --> C[inventories/]
    C --> C1[dev/]
    C1 --> C1a[hosts.yml]
    C1 --> C1b[group_vars/]
    C1 --> C1c[docs/]
    C --> C2[prod/]
    C2 --> C2a[hosts.yml]
    C2 --> C2b[group_vars/]

    A --> D[roles/]
    D --> D1[postgresql/]
    D1 --> D1a[tasks/]
    D1 --> D1b[vars/]
    D1 --> D1c[templates/]
    D --> D2[nginx/]
    D2 --> D2a[tasks/]
    D2 --> D2b[vars/]
    D2 --> D2c[templates/]

    A --> E[playbooks/]
    E --> E1[db-setup.yml]
    E --> E2[web-deploy.yml]

    A --> F[awx/]
    F --> F1[templates/]
    F --> F2[configs/]

