


[Command to reset ArgoCD's password](https://github.com/argoproj/argo-cd/blob/master/docs/faq.md#i-forgot-the-admin-password-how-do-i-reset-it)
```
kubectl -n argocd patch secret argocd-secret \
  -p '{"stringData": {
    "admin.password": "$2a$10$YnMhclxGKAl61DiUM..wYum9feNvcfCNHXheoW8n90Ut6OrKI3fFm",
    "admin.passwordMtime": "'$(date +%FT%T%Z)'"
  }}'
```


[nginx-ingress-controller](https://quay.io/repository/kubernetes-ingress-controller/nginx-ingress-controller-arm64?tab=tags)