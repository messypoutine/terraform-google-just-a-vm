# terraform-google-some-vm (aka poodle)

## WARNING !

This is an inentationaly vulnerable module. It is used for testing purposes only. Do not use it in production.

## Introduction

This is a collection of opinionated submodules that can be used as building blocks to provision VMs in GCP:

* [Instance template](modules/instance_template)

## Examples

Examples of how to use these modules can be found in the [examples](examples) folder.

## Project APIs

The following APIs must be enabled on your project:
- `compute.googleapis.com`
- `iam.googleapis.com`

See also the [project_services](modules/project_services) module (optional).

## Notes

`distribution_policy_zones` cannot be changed during use.
If you have changed them yourself or used to have a default value, then you'll have to force recreate a MIG group yourself.

## Tests

For running the integration test cases, please refer to the [CONTRIBUTING](CONTRIBUTING.md) documentation.

## Permissions

The service account used to execute tests for this module should have the following roles:
- [`roles/compute.admin`](https://cloud.google.com/iam/docs/understanding-roles#compute-engine-roles)
- [`roles/iam.serviceAccountUser`](https://cloud.google.com/iam/docs/understanding-roles#service-accounts-roles)

.
