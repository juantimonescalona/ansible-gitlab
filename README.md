# Ansible Skeleton

This is a base directory layout for ansible playbooks. It is based in the best practices recomendations by ansible http://docs.ansible.com/ansible/playbooks_best_practices.html#directory-layout.

## Useful ansible commands

Run main playbook in local environment

```
ansible-playbook -i local main.yml
```

Run main playbook in production environment

```
ansible-playbook -i production main.yml
```

Run main playbook in production environment, just spain country. To enable this, is useful to separate servers by country

```
ansible-playbook -i production main.yml -l *_es
```

Run main playbook adding input variables

```
ansible-playbook -i production main.yml --extra-vars "version=1.0.0"
```
