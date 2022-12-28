Set up a 3 node HA rancher cluster. 

This will create and prep nodes for RKE. This uses the default vpc and subnets. 

We create:

* SSH Key Pair
* Security Groups
* 3 Instances
* ELB for 80/443 points to the 3 instances.
* Route53 DNS pointed to ELB

Outputs: address and internal_address values for RKE

You will need terraform and aws-cli installed.

Copy all these files down to a directory and run 'terraform apply'. You will be prompted for the variable values.

## Next Steps
Take the provided `address` and `internal_address` and populate the appropriate section in the rke `cluster.yml` then run rke up.


# test_terraform_rancher_k8s
