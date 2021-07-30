---
title: "Boto3 Explorations"
date: 2021-07-26T14:12:52-07:00
---
An Amazon EC2 security group acts as a virtual firewall that controls the traffic for one or more instances. You add rules to each security group to allow traffic to or from its associated instances. You can modify the rules for a security group at any time; the new rules are automatically applied to all instances that are associated with the security group.

In this example, Python code is used to perform several Amazon EC2 operations involving security groups. The code uses the AWS SDK for Python to manage IAM access keys using these methods of the EC2 client class:

{{< highlight python "linenos=true" >}}

response = client.allocate_address(
    Domain='vpc'|'standard',
    Address='string',
    PublicIpv4Pool='string',
    NetworkBorderGroup='string',
    CustomerOwnedIpv4Pool='string',
    DryRun=True|False,
    TagSpecifications=[
        {
            'ResourceType': 'client-vpn-endpoint'|'customer-gateway'|'dedicated-host'|'dhcp-options'|'egress-only-internet-gateway'|'elastic-ip'|'elastic-gpu'|'export-image-task'|'export-instance-task'|'fleet'|'fpga-image'|'host-reservation'|'image'|'import-image-task'|'import-snapshot-task'|'instance'|'instance-event-window'|'internet-gateway'|'key-pair'|'launch-template'|'local-gateway-route-table-vpc-association'|'natgateway'|'network-acl'|'network-interface'|'network-insights-analysis'|'network-insights-path'|'placement-group'|'reserved-instances'|'route-table'|'security-group'|'security-group-rule'|'snapshot'|'spot-fleet-request'|'spot-instances-request'|'subnet'|'traffic-mirror-filter'|'traffic-mirror-session'|'traffic-mirror-target'|'transit-gateway'|'transit-gateway-attachment'|'transit-gateway-connect-peer'|'transit-gateway-multicast-domain'|'transit-gateway-route-table'|'volume'|'vpc'|'vpc-peering-connection'|'vpn-connection'|'vpn-gateway'|'vpc-flow-log',
            'Tags': [
                {
                    'Key': 'string',
                    'Value': 'string'
                },
            ]
        },
    ]
)
{{< / highlight >}}
