# {{cookiecutter.role_name | upper}}
{% for letter in cookiecutter.role_name %}={% endfor %}

{{cookiecutter.short_description}}


## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: redbeard28.{{cookiecutter.short_name}}
````

More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible {{cookiecutter.ansible_version}}+


Role Variables
--------------

```yaml
---
# Put role variables
```

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redbeard28.{{cookiecutter.short_name}}, tags: mytags }


Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
image=debian tag="buster" molecule converge 
image=debian tag="buster" molecule verify 
```

Author Information
------------------

{{cookiecutter.author_name}}[¹](mailto:{{cookiecutter.author_email}}) from {{cookiecutter.Compagny_name}}
