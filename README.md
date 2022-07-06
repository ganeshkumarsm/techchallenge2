# techchallenge2

Assumptions:
===============
1. Ansible is installed on the Control Node on Linux. 
2. Install jmespath on the Control node using command: pip install jmespath
3. Managed node is on Linux deployed on AWS.
4. Python (2.6 or later/3.5 or later) is installed on the control Node and the managed node.
5. All the basic requirements for the Ansible control node to communication with Managed node is taken care (Ansadmin, SSH, keys etc)
6. Make sure the hosts file contains the managed nodes's IP addressess before running the playbookd.

How to Steps:
================
1. Copy the Ansible playbook yml file to the control node. 
2. Login to the control node using ansadmin user.
3. Goto the location which contains the playbook yml file.
4. Run the command ansible-playbook AWS_EC2_Instance_metadata.yml
5. We can see the results as a JSON output and individual metadata item for each managed node.

 Output snippet: Filtered Individual metadata of each node:
 ============================================================

TASK [Display filtered individual metadata of each node as a list] ************************************************************************************************************************************************
ok: [172.31.7.57] => {
    "each_node_filtered_meta": [
        "ami-079b5e5b3971bd10d",
        "0",
        "(unknown)",
        "ami\nroot",
        "maintenance/",
        "ip-172-31-7-57.ap-south-1.compute.internal",
        "ec2/",
        "none",
        "i-0f51451f40f14d3ba",
        "on-demand",
        "t2.micro",
        "ip-172-31-7-57.ap-south-1.compute.internal",
        "172.31.7.57",
        "0a:5c:3b:c1:1f:3a",
        "vhostmd",
        "interfaces/",
        "availability-zone\navailability-zone-id\nregion",
        "default-hvm",
        "ec2-3-7-45-134.ap-south-1.compute.amazonaws.com",
        "3.7.45.134",
        "0=aws_key",
        "r-0eb09f925949e3340",
        "launch-wizard-2",
        "domain\npartition"
    ]
}

