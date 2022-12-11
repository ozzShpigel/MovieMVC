# AzureTest

azure secret 1kS8Q~ZaOjhYLrYmk1MFy5ggDtXu9hToZNSn5afk
azure id a2d6a1db-0409-42ab-bdee-39f86b4ea704
tenent id 6204eec6-93d2-419a-b86f-95faa7d43f8e
subscription id e1a5d97b-66c1-4626-8614-562e33c33b61


$ARM_CLIENT_ID="a2d6a1db-0409-42ab-bdee-39f86b4ea704"
$ARM_CLIENT_SECRET="1kS8Q~ZaOjhYLrYmk1MFy5ggDtXu9hToZNSn5afk"
$ARM_TENANT_ID="6204eec6-93d2-419a-b86f-95faa7d43f8e"
$ARM_SUBSCRIPTION_ID="e1a5d97b-66c1-4626-8614-562e33c33b61"
az login --service-principal -u $ARM_CLIENT_ID -p $ARM_CLIENT_SECRET --tenant $ARM_TENANT_ID --subscription $ARM_SUBSCRIPTION_ID

az account set --subscription $ARM_SUBSCRIPTION_ID


terraform plan -var tenant_id=$ARM_TENANT_ID -var client_id=$ARM_CLIENT_ID -var client_secret=$ARM_CLIENT_SECRET -var subscription_id=$ARM_SUBSCRIPTION_ID 

terraform apply --auto-approve -var tenant_id=$ARM_TENANT_ID -var client_id=$ARM_CLIENT_ID -var client_secret=$ARM_CLIENT_SECRET -var subscription_id=$ARM_SUBSCRIPTION_ID 