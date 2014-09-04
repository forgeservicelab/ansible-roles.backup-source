Backup Source
=============

Grants SSH access to a backup client.
Ensures RSYNC is available on the target machine.

Role Variables
--------------

- `source_user` - Name of an existing user on the target machine. SSH access as this user will be granted. If not set, a system user with the name of `replicator` will be created.
- `backup_client_pubkey` - path to the public key being granted access defaults to `~/.ssh/id_rsa.pub`.

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: backup-source, backup_client_pubkey: ~/.ssh/id_rsa.pub }

Author Information
------------------

Jorge Rodriguez.
