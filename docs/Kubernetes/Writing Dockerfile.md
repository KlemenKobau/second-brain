## SIGTERM
Make sure to pass **SIGTERM** to the application!
**Alpine linux** does not pass it with the default shell!
Use:
```bash
CMD [ "myapp" ]
```
OR:
```bash
CMD [ "/bin/bash", "-c", "myapp --arg=$ENV_VAR" ]
```

### Note for kubernetes
Nginx exits violently on **SIGTERM**, it does not exit gracefully!
Use **preStop hooks**

```yaml
apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: nginx
spec:
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
        ports:
        - containerPort: 80
        lifecycle:
          preStop:
            exec:
              # SIGTERM triggers a quick exit; gracefully terminate instead
              command: ["/usr/sbin/nginx","-s","quit"]
```

[original blog from Marco Pracucci](https://pracucci.com/graceful-shutdown-of-kubernetes-pods.html)