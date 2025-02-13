# CrashLoopBackOff

## Issue Summary

`CrashLoopBackOff` is a Kubernetes state representing a restart loop that's happening in a Pod where a container in the Pod is started, but crashes and is then restarted, over and over again

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/More%20Assets/Screenshot%202024-12-16%20220824.png)

- Kubernetes will wait and will increase the back-off time between restarts to give you a chance to fix the error
- This state means that it's currently waiting for the indicated time before restarting the Pod again, which will probably fail again unless the problem has been fixed

## Error Messages

```Text
Container keeps crashing.
```
<br>

```Text
Can’t restart some containers in this Pod.
```
<br>

```Text
Kubernetes restarts the Pods with an exponential delay starting at 10 seconds, for a maximum of 5 minutes, until the Pods run successfully for 10 minutes. If a problem prevents the Pods from running, your services might experience prolonged downtime.
```
<br>

```Bash
$ kubectl get pods
NAME                     READY     STATUS             RESTARTS   AGE
<POD_ID>                 0/1       CrashLoopBackOff   1>          1m
```
<br>

```Text
"Back-off restarting failed container <CONTAINER_ID> in pod <POD_ID>"
```
  
![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
