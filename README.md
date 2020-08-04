## Control verge.io cluster via Ansible

Utilizes Ansible's uri module to control the verge.io API.

Instructions:

Add your tenant UI FQDNs in the inventory file under the [verge_tenants] option.
Add users to the "loop" section of verge.yml

Run "ansible-playbook verge.yml"

You will be asked for username and password of a verge.io user capable of using the API.

## Notes: 

This assumes you have an external already-configured auth_source. For local accounts, you will need to make modifications.
This runs on the localhost where ansible is run from, which needs to reach the UI
It assumes that the verge.io API doesn't have a valid cert, so cert checks are disabled.

