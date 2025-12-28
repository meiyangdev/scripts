terragrunt import
```
aws sts get-caller-identity
terragrunt import aws_iam_role.datadog_integration_role DatadogIntegrationRole
terragrunt plan
```
terragrunt plan
```
terragrunt plan -out a.plan
terragrunt apply a.plan
 
terragrunt plan -no-color > ./new_plan.txt save to current folder
grep -i destroy new_plan.txt | grep -i queue
grep -i destroy tax_plan.txt | grep -i queue | grep dead_letter_queue
```
terragrunt state list
```
terragrunt state list
terragrunt state show `state-list-name`
```
terragrunt remove state
```
terragrunt state rm aws_route53_record.mx_test_com
```
terragrunt target destroy
```
terragrunt destroy -target=aws_db_instance.replicaencrypted[0]
```
