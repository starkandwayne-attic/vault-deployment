Vault Deployment Template
======================================

This repository acts as an upstream repository of YAML templates for use
in deploying one or more Vault clusters, via the [Gensis][1] utility.



Creating a new Vault Deployment
======================================

To create a new [Genesis][1]-based deployment of Vault, run

    genesis new deployment --template vault

This will create a new repo called `vault-deployments` for you, and
pull in the `github.com/starkandwayne/vault-deployment` repo as the
`upstream` remote, copying the contents of `global/*` into the new
`vault-deployments` repository.

This allows you to easily diverge from the upstream templates to suit your
environment, yet still be able to pull in changes from upstream down
the road.



BOSH-Lite Sites
======================================

The `bosh-lite` template will set you up with a structure suitable
for deploying Vault on a BOSH-Lite.

    genesis new site --tempalte bosh-lite <name>



vSphere Sites
======================================

The `vsphere` template will set you up with a structure suitable
for deploying Vault on a VMWare vSphere ESXi cluster.

    genesis new site --template vsphere <name>



Amazon EC2 (AWS) Sites
======================================

The `aws` template will set you up with a structure suitable for
deploying Vault to Amazon Web Service's EC2/VPC
infrastructure.

    genesis new site --template aws <name>



Notes
======================================

For more information, check out the [Genesis][1] repo, or `genesis help`.
You can download the Genesis program from [Github][1]



[1]: https://github.com/starkandwayne/genesis
