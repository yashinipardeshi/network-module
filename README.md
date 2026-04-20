# 2-Tier Network Module

Complete Azure network infrastructure for 2-tier architecture (AppGW → VMSS → SQL).

## Features
- ✅ VNet + 3 Subnets (AppGW/VMSS/DB)
- ✅ NSGs with exact security rules
- ✅ SQL Private Endpoint + DNS Zone
- ✅ Production-ready defaults

## Usage
```hcl
module "network" {
  source = "YOUR-ORG/network/azurerm"

  resource_group_name = azurerm_resource_group.rg.name
  location           = azurerm_resource_group.rg.location
  sql_server_id      = azurerm_mssql_server.sql.id
}