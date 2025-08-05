# GitOps Directory Structure for GitOps Fix Test Fabric

This directory contains the GitOps file management structure for the Hedgehog fabric "GitOps Fix Test Fabric".

## Directory Structure

- **raw/**: Drop YAML files here for processing by HNP
- **managed/**: HNP-managed normalized files organized by CRD type
- **unmanaged/**: Files that exist in the repository but are not managed by HNP
- **.hnp/**: HNP metadata and configuration files

## How It Works

1. Drop your YAML files in the `raw/` directory
2. HNP will process them and create normalized files in `managed/`
3. Original files will be archived according to the configured strategy
4. HNP maintains metadata in the `.hnp/` directory

## Managed CRD Types

The `managed/` directory contains subdirectories for each supported CRD type:

- connections/
- servers/
- switches/
- switchgroups/
- vlannamespaces/
- vpcs/
- externals/
- externalattachments/
- externalpeerings/
- ipv4namespaces/
- vpcattachments/
- vpcpeerings/

## Generated

This structure was created by Hedgehog NetBox Plugin on 2025-08-05 04:03:14 UTC.
