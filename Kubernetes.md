# CrashLoopBackOff

Issue Summary: `CrashLoopBackOff` is a Kubernetes state representing a restart loop that's happening in a Pod where a container in the Pod is started, but crashes and is then restarted, over and over again

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/More%20Assets/Screenshot%202024-12-16%20220824.png)

- Kubernetes will wait and will increase the back-off time between restarts to give you a chance to fix the error
- This state means that it's currently waiting for the indicated time before restarting the Pod again, which will probably fail again unless the problem has been fixed

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
