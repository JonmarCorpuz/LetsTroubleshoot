# Forces Replacement Error Overview

A `Forces replacement` message refers to a situation where changes to the configuration or updates to resource properties require the destruction and recreation of the resource instead of an in-place update

* This typically happens when a change affects an immutable property of a resource (Meaning that the property can't be changed once the resource is created without recreating the resource)

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common Error Messages

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Sources

* https://stackoverflow.com/a/68945937
* https://github.com/hashicorp/terraform-provider-google/issues/15148#issuecomment-1652315422
* https://github.com/hashicorp/terraform-provider-google/issues/12620
