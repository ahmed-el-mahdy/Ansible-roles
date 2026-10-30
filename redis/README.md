Role Name
=========

Redis package/service/configuration role. Source review: 30 October 2026. Installs `redis-server` on Debian or `redis` on RedHat, enables the corresponding service and writes `requirepass` from `redis_password`. Read the root README for the current entry-point and security boundaries.

Requirements
------------

An authorized inventory, compatible Linux host, appropriate privilege escalation and a caller playbook are required. The root playbook is currently empty. Test handler and configuration-path compatibility on a disposable target before use.

Role Variables
--------------

`redis_password` is required as a private input. Do not put its value in Git, command history, logs or a public check diff. The repository's file named `vars/vault.yml` is not proof of encryption or populated credentials. Review the copy task: it replaces the configuration rather than preserving all pre-existing options.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
