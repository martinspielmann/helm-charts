# azure-apps

![Version: 0.2.2](https://img.shields.io/badge/Version-0.2.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

Argo CD app-of-apps config for Azure applications

**Homepage:** <https://github.com/adfinis-sygroup/helm-charts/tree/master/charts/azure-apps>

## Maintainers
This chart is maintained by [Adfinis](https://adfinis.com/?pk_campaign=github&pk_kwd=helm-charts).

## Source Code

* <https://github.com/adfinis-sygroup/helm-charts>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.adfinis.com | argoconfig | 0.7.4 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| azureKvCsiProvider | object | - | [secrets-store-csi-driver-provider-azure](https://github.com/Azure/secrets-store-csi-driver-provider-azure) ([example](./examples/secrets-store-csi-driver-provider-azure.yaml)) |
| azureKvCsiProvider.chart | string | `"csi-secrets-store-provider-azure"` | Chart |
| azureKvCsiProvider.destination.namespace | string | `"kube-system"` | Namespace |
| azureKvCsiProvider.enabled | bool | `false` | Enable secrets-store-csi-driver-provider-azure |
| azureKvCsiProvider.repoURL | string | [repo](https://raw.githubusercontent.com/Azure/secrets-store-csi-driver-provider-azure/master/charts) | Repo URL |
| azureKvCsiProvider.targetRevision | string | `"0.2.*"` | [vault-csi-provider-azure Helm chart](https://github.com/Azure/secrets-store-csi-driver-provider-azure/tree/master/charts/csi-secrets-store-provider-azure) version |
| azureKvCsiProvider.values | object | [upstream values](https://github.com/Azure/secrets-store-csi-driver-provider-azure/blob/master/charts/csi-secrets-store-provider-azure/values.yaml) | Helm values |
| promitorResourceDiscovery | object | - | [promitor](https://promitor.io/) resource discovery ([example](./examples/promitor.yaml)) |
| promitorResourceDiscovery.chart | string | `"promitor-agent-resource-discovery"` | Chart |
| promitorResourceDiscovery.destination.namespace | string | `"infra-promitor"` | Namespace |
| promitorResourceDiscovery.enabled | bool | `false` | Enable promitor resource discovery |
| promitorResourceDiscovery.repoURL | string | [repo](https://charts.promitor.io) | Repo URL |
| promitorResourceDiscovery.targetRevision | string | `"0.6.*"` | [promitor-agent-resource-discovery Helm chart](https://github.com/promitor/charts/tree/main/promitor-agent-resource-discovery) version |
| promitorResourceDiscovery.values | object | [upstream values](https://github.com/promitor/charts/blob/main/promitor-agent-resource-discovery/values.yaml) | Helm values |
| promitorScraper | object | - | [promitor](https://promitor.io/) scraper ([example](./examples/promitor.yaml)) |
| promitorScraper.chart | string | `"promitor-agent-scraper"` | Chart |
| promitorScraper.destination.namespace | string | `"infra-promitor"` | Namespace |
| promitorScraper.enabled | bool | `false` | Enable promitor scraper |
| promitorScraper.repoURL | string | [repo](https://charts.promitor.io) | Repo URL |
| promitorScraper.targetRevision | string | `"2.6.*"` | [promitor-agent-scraper Helm chart](https://github.com/promitor/charts/tree/main/promitor-agent-scraper) version |
| promitorScraper.values | object | [upstream values](https://github.com/promitor/charts/blob/main/promitor-agent-scraper/values.yaml) | Helm values |

## About this chart

Adfinis fights for a software world that is more open, where the quality is
better and where software must be accessible to everyone. This chart
is part of the action behind this commitment. Feel free to
[contact](https://adfinis.com/kontakt/?pk_campaign=github&pk_kwd=helm-charts)
us if you have any questions.

## License

This Helm chart is free software: you can redistribute it and/or modify it under the terms
of the GNU Affero General Public License as published by the Free Software Foundation,
version 3 of the License.

----------------------------------------------
Autogenerated from chart metadata using [helm-docs](https://github.com/norwoodj/helm-docs/)