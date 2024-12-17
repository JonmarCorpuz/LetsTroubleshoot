# ImagePullBackOff Overview

ImagePullBackOff means that the Pod cannot start because the container image cannot be pulled from the registry after retrying several times

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common ImagePullBackOff Causes

## Networking Related Causes

[ ] Incorrect registry URL 
[ ] Unreachable registry URL
[ ] Something is blocking the connection to the registry (*Firewall rule*, *Network configuration*, *etc.*)
[ ] The proxy settings aren't configured properly

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Debugging ImagePullBackOff

