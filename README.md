# Infra3

> This app is compliant with version [2.1.1](https://github.com/policy-as-versioned-code/policy/releases/tag/2.1.1) of the company policy

## Test policy locally

```raw
$ docker run --rm -ti -v $(pwd):/apps ghcr.io/policy-as-versioned-code/policy-checker
Found Terraform files
Checking policy version...
/tmp/tf/main.tf
/tmp/tf/variable.tf
/tmp/tf/CODE_OF_CONDUCT.md
/tmp/tf/SECURITY.md
/tmp/tf/README.md
Policy version: 2.1.1
Fetching Policy...
Policy fetched.
Running policy checker...

       _               _
   ___| |__   ___  ___| | _______   __
  / __| '_ \ / _ \/ __| |/ / _ \ \ / /
 | (__| | | |  __/ (__|   < (_) \ V /
  \___|_| |_|\___|\___|_|\_\___/ \_/

By bridgecrew.io | version: 2.0.1140

terraform scan results:

Passed checks: 3, Failed checks: 0, Skipped checks: 0

Check: : ""
	PASSED for resource: aws_s3_bucket.b
	File: /main.tf:1-6
Check: CUSTOM_AWS_2: "Check that all resources are tagged with the key - department with a known value"
	PASSED for resource: aws_s3_bucket.b
	File: /main.tf:1-6
Check: CUSTOM_AWS_1: "Check that all resources are tagged with the key - department"
	PASSED for resource: aws_s3_bucket.b
	File: /main.tf:1-6
```