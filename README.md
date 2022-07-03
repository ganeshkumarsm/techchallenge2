# techchallenge2

Assumptions:
===============
1. Ansible is installed on the Control Node on Linux. 
2. Managed node is on Linux deployed on AWS.
3. Python (2.6 or later/3.5 or later) is installed on the control Node and the managed node.
4. All the basic requirements for the Ansible control node to communication with Managed node is taken care (Ansadmin, SSH, keys etc)
5. Make sure the hosts file contains the managed nodes's IP addressess before running the playbookd.

How to Steps:
================
1. Copy the Ansible playbook yml file to the control node. 
2. Login to the control node using ansadmin user.
3. Goto the location which contains the playbook yml file.
4. Run the command ansible-playbook <yml file name>
5. We can see the results as a JSON output.
