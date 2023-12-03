# AWS OpenSearch Serverless Terraform module

Terraform module which creates AWS OpenSearch Serverless resources.

## Usage

See [`examples`](https://github.com/terraform-aws-modules/terraform-aws-opensearch/tree/master/examples) directory for working examples to reference:

```hcl
module "opensearch_serverless" {
  source = "terraform-aws-modules/opensearch/aws//modules/serverless"

  tags = {
    Terraform   = "true"
    Environment = "dev"
  }
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 5.24 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | >= 5.24 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_opensearchserverless_collection.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/opensearchserverless_collection) | resource |
| [aws_opensearchserverless_security_policy.encryption](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/opensearchserverless_security_policy) | resource |
| [aws_opensearchserverless_security_policy.network](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/opensearchserverless_security_policy) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_create"></a> [create](#input\_create) | Determines whether resources will be created (affects all resources) | `bool` | `true` | no |
| <a name="input_create_encryption_policy"></a> [create\_encryption\_policy](#input\_create\_encryption\_policy) | Determines whether an encryption policy will be created | `bool` | `true` | no |
| <a name="input_create_network_policy"></a> [create\_network\_policy](#input\_create\_network\_policy) | Determines whether an network policy will be created | `bool` | `true` | no |
| <a name="input_description"></a> [description](#input\_description) | Description of the collection | `string` | `null` | no |
| <a name="input_encryption_security_policy"></a> [encryption\_security\_policy](#input\_encryption\_security\_policy) | Encryption security policy to apply to the collection - this is merged with the default policy provided | `any` | `{}` | no |
| <a name="input_encryption_security_policy_description"></a> [encryption\_security\_policy\_description](#input\_encryption\_security\_policy\_description) | Description of the encryption security policy | `string` | `null` | no |
| <a name="input_encryption_security_policy_name"></a> [encryption\_security\_policy\_name](#input\_encryption\_security\_policy\_name) | Name of the encryption security policy | `string` | `null` | no |
| <a name="input_name"></a> [name](#input\_name) | Name of the collection | `string` | `""` | no |
| <a name="input_network_security_policy"></a> [network\_security\_policy](#input\_network\_security\_policy) | Network security policy to apply to the collection - this is merged with the default policy provided | `any` | `{}` | no |
| <a name="input_network_security_policy_description"></a> [network\_security\_policy\_description](#input\_network\_security\_policy\_description) | Description of the network security policy | `string` | `null` | no |
| <a name="input_network_security_policy_name"></a> [network\_security\_policy\_name](#input\_network\_security\_policy\_name) | Name of the network security policy | `string` | `null` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | A map of tags to add to all resources | `map(string)` | `{}` | no |
| <a name="input_timeouts"></a> [timeouts](#input\_timeouts) | Create and delete timeout configurations for the collection | `map(string)` | `{}` | no |
| <a name="input_type"></a> [type](#input\_type) | Type of collection. One of `SEARCH`, `TIMESERIES`, or `VECTORSEARCH`. Defaults to `TIMESERIES` | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_arn"></a> [arn](#output\_arn) | Amazon Resource Name (ARN) of the collection |
| <a name="output_dashboard_endpoint"></a> [dashboard\_endpoint](#output\_dashboard\_endpoint) | Collection-specific endpoint used to access OpenSearch Dashboards |
| <a name="output_encryption_security_policy"></a> [encryption\_security\_policy](#output\_encryption\_security\_policy) | The JSON policy document of the security policy |
| <a name="output_encryption_security_policy_version"></a> [encryption\_security\_policy\_version](#output\_encryption\_security\_policy\_version) | The version of the security policy |
| <a name="output_endpoint"></a> [endpoint](#output\_endpoint) | Collection-specific endpoint used to submit index, search, and data upload requests to an OpenSearch Serverless collection |
| <a name="output_id"></a> [id](#output\_id) | Unique identifier for the collection |
| <a name="output_kms_key_arn"></a> [kms\_key\_arn](#output\_kms\_key\_arn) | The ARN of the Amazon Web Services KMS key used to encrypt the collection |
| <a name="output_network_security_policy"></a> [network\_security\_policy](#output\_network\_security\_policy) | The JSON policy document of the security policy |
| <a name="output_network_security_policy_version"></a> [network\_security\_policy\_version](#output\_network\_security\_policy\_version) | The version of the security policy |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## License

Apache-2.0 Licensed. See [LICENSE](https://github.com/terraform-aws-modules/terraform-aws-opensearch/blob/master/LICENSE).