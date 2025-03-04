---
title: Restart server - Azure CLI - Azure Database for MySQL
description: This article describes how you can restart an Azure Database for MySQL server using the Azure CLI.
ms.service: mysql
ms.subservice: single-server
author: savjani
ms.author: pariks
ms.topic: how-to
ms.date: 06/20/2022
ms.custom: devx-track-azurecli
---

# Restart Azure Database for MySQL server using the Azure CLI

[!INCLUDE[applies-to-mysql-single-server](../includes/applies-to-mysql-single-server.md)]
This topic describes how you can restart an Azure Database for MySQL server. You may need to restart your server for maintenance reasons, which causes a short outage as the server performs the operation.

The server restart will be blocked if the service is busy. For example, the service may be processing a previously requested operation such as scaling vCores.

The time required to complete a restart depends on the MySQL recovery process. To decrease the restart time, we recommend you minimize the amount of activity occurring on the server prior to the restart.

## Prerequisites

To complete this how-to guide:

- You need an [Azure Database for MySQL server](quickstart-create-server-up-azure-cli.md).
 
[!INCLUDE [azure-cli-prepare-your-environment-no-header.md](../../../includes/azure-cli-prepare-your-environment-no-header.md)]

- This article requires version 2.0 or later of the Azure CLI. If using Azure Cloud Shell, the latest version is already installed.

## Restart the server

Restart the server with the following command:

```azurecli-interactive
az mysql server restart --name mydemoserver --resource-group myresourcegroup
```

## Next steps

Learn about [how to set parameters in Azure Database for MySQL](how-to-configure-server-parameters-using-cli.md)
