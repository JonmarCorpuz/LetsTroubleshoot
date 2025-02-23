# Failed to Construct REST Client Error Overview

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common Error Messages

```Text
Error: Failed to construct REST client

cannot create REST client: no client config
```

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common Causes

* "The kubernetes_manifest resource needs access to the API server of the cluster during planning. This is because, in order to support CRDs in Terraform ecosystem, we need to pull the schema information for each manifest resource at runtime (during planing)." (https://github.com/hashicorp/terraform-provider-kubernetes/issues/1775#issuecomment-1193859982)

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common Symptoms

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Potential Workarounds
