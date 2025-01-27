# terraform-aviatrix-mc-firenet release notes

## v1.1.1
- Add support for deploying Aviatrix FQDN egress filtering gateways in Azure and GCP.
    - Known issue: Azure firenet subnets are not created deterministically, causing potential issue with deploying FQDN gateway in the wrong subnet.
- Automatically truncate VPC name to 30 characters

## v1.1.0
- Made module compatioble with controller version 6.7 and provider version 2.22.x.
- Made firewall instance association conditional with new boolean argument `associated`.
- Resolved a bug where FQDN egress gateways could not be deployed in other clouds than AWS.

## v1.0.2
- Fixed a bug where firewall instances in Azure were not deployed to AZ's (Credits: Andreas Krummrich, SVA)

## v1.0.1
- Add examples
- Add input validation for fw_amount
- Change variables with a default value to non-nullable to prevent overwriting internal logic when setting input to null on partent/root module.

## v1.0.0
Initial release