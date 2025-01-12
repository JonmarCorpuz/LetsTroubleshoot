# Error Messages

```Text
Error: Failed to construct REST client

cannot create REST client: no client config
```

# Root Cause

* "The kubernetes_manifest resource needs access to the API server of the cluster during planning. This is because, in order to support CRDs in Terraform ecosystem, we need to pull the schema information for each manifest resource at runtime (during planing)." (https://github.com/hashicorp/terraform-provider-kubernetes/issues/1775#issuecomment-1193859982)

# Workarounds

# Solutions
