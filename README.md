# Ansible Assignment: hw-14

I created this repo for DevOps Experts bootcamp homework, as instructed by my teacher Doron Nuni

## Project Structure

```
hw-14/
├── inventory
├── playbook.yml
└── roles/
    ├── common/
    │   └── tasks/
    │       └── main.yml
    ├── deploy_file/
    │   └── tasks/
    │       └── main.yml
    └── deploy_template/
        ├── tasks/
        │   └── main.yml
        └── templates/
            └── test2.j2
```

## Roles

### 1. Common
Installs vim and zip on all servers.

### 2. Deploy File
Deploys a file with the content "Hello world!" to `/tmp/test1` on all hosts.

### 3. Deploy Template
Deploys a template file to `/tmp/test2` on all hosts, containing the server's hostname.

## Inventory

The `inventory` file contains the list of servers to be managed. Make sure to update this file with your actual server details.

## Playbook

The `playbook.yml` file orchestrates the application of all roles to the servers specified in the inventory.

## Usage

To run the playbook:

1. Ensure Ansible is installed on your control node/local machine.
2. Update the `inventory` file with your server details.
3. Run the playbook with the following command:

   ```
   ansible-playbook -i inventory playbook.yml
   ```

## Requirements

- Ansible 2.9 or higher
- SSH access to the target servers
- Sudo privileges on the target servers
