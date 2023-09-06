# argocd-local-deployments
confgurations for apps to be deployed on ArgoCD

## Set Up
- [Install](https://argo-cd.readthedocs.io/en/stable/getting_started/) ArgoCD

- Start Docker Desktop

- Fetch ArgoCD password
```bash
$ argocd admin initial-password -n argocd
```

- Start ArgoCD server
```bash
$ kubectl port-forward svc/argocd-server -n argocd 8080:443
```

- Deploy the app to ArgoCD by running,
```bash
$ kubectl apply  -f <argocd-deployment-config>.yaml
```

- Manually synchronize by clicking on the *Sync* button
<img width="1349" alt="image" src="https://github.com/Mbaoma/fastAPI/assets/49791498/e142a376-02ad-4b78-8e94-3ef097764083">

- Healthy deployment
<img width="1349" alt="image" src="https://github.com/Mbaoma/fastAPI/assets/49791498/6c4c4a12-c5b5-4fef-a502-317f52f19fe0">

- Access the app by clicking on the created pod, and then logs
<img width="1349" alt="image" src="https://github.com/Mbaoma/fastAPI/assets/49791498/fcc05246-9d48-49c4-9191-d49cf9eece4c">

