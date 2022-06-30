# Training engineer

## Homework 13 - Aws and Ansible and Docker

### Instructions

Написать Ansible playbook, который разворачивает 2 ноды в AWS
EC2: сборочную и продовую. На сборочной ноде происходит
сборка Java проекта, полученный артефакт передается на
продовую ноду и на ней запускается.

### Tips

Tested on:

- Ubuntu Ubuntu 20.04.4 LTS
- Ansible 2.9.6
- Python 3.8.10

### Pre


    $ ssh-keygen
    ...

    $ ansible-vault create vars.vault
    ...
    aws_access_key: SUPERSECRETIDHERE
    aws_secret_key: SUPERSECRETKEYHERE
    dockerhub_user: SUPERSECRETLOGINHERE
    dockerhub_pass: SUPERSECRETPASSWORDHERE

    $ ansible-playbook main.yml --ask-vault-pass
