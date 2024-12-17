# CrashLoopBackOff Overview

CrashLoopBackOff is a Kubernetes state representing a restart loop that's happening in a Pod where a container in the Pod is started, but crashes and is then restarted, over and over again

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/More%20Assets/Screenshot%202024-12-16%20220824.png)

* Kubernetes will wait an increasing back-off time between restarts to give you a chance to fix the error
* When a Pod state is displaying CrashLoopBackOff, it means that it’s currently waiting the indicated time before restarting the pod again (It will probably fail again, unless it’s fixed)

## CrashLoop

* CrashLoopBackOff is not an error on itself, but indicates that there’s an error happening that prevents a Pod from starting properly
* The reason why it’s restarting is because its `restartPolicy` is set to `Always` (by default) or `OnFailure`, and the kubelet is then reading this configuration and restarting the containers in the Pod and causing the loop
* CrashLoopBackOff is useful since it provides us some time for missing resources to finish loading, as well as for us to detect the problem and debug it

## BackOff

The BackOff part is an exponential delay between restarts (Between a few seconds and five minutes)

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Error Messages

```Text
Container keeps crashing.
```

```Text
Can’t restart some containers in this Pod.
```

```Text
Kubernetes restarts the Pods with an exponential delay starting at 10 seconds, for a maximum of 5 minutes, until the Pods run successfully for 10 minutes. If a problem prevents the Pods from running, your services might experience prolonged downtime.
```

```Bash
$ kubectl get pods
NAME                     READY     STATUS             RESTARTS   AGE
<POD_ID>                 0/1       CrashLoopBackOff   1>          1m
```

```Bash
"Back-off restarting failed container"
```

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Common CrashLoopBackOff Causes

## Application Related CrashLoopBackOff Causes

- [ ] Misconfigurations (*Typos*, *etc.*)
- [ ] A resource is not available (*PersistentVolume not mounted*, *etc.*)
- [ ] Wrong command line arguments (*Missing arguments*, *Incorrect arguments*, *etc.*)
- [ ] A lack of permissions (*Read-only filesystem*, *etc.*)

## Network Related CrashLoopBackOff Causes

- [ ] You tried to bind an existing port
- [ ] Memory limits are too low (the container is Out Of Memory killed)
- [ ] Liveness probes aren't reporting the Pod as ready

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# Debugging CrashLoopBackOff

## Check Pod Description

```Bash
kubectl describe pod <POD_ID>
```

## Check Pod Logs

```Bash
kubectl logs <POD_ID> --all-containers
```

## Check Container Logs

```Bash
kubectl logs <POD_ID> -c <CONTAINER_ID>
```

## Check Pod Events

```Bash
kubectl get events
```

```Bash
kubectl get events --field-selector involvedObject.name=<POD_ID>
```

## Check Deployment

```Bash
kubectl describe deployment <DEPLOYMENT_NAME>
```
