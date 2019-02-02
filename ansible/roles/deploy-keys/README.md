Role Name
=========

Deploy public ssk key .

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
        - { role: deploy-keys, vars: { become: yes, become_user: root }, tags: ["pubkey"] }

License
-------

BSD