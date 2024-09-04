# GitHub Integration

Kadras Developer Portal provides out-of-the-box integration with GitHub. Before installing this package, you need to configure the necessary credentials to use your GitHub organization.

Define a Secret with a GitHub Personal Access Token (PAT) that will be used by the Scaffolder, and a client ID/client secret pair associated to a GitHub App that will be used by the authentication provider.

```shell
apiVersion: v1
kind: Secret
metadata:
  name: developer-portal-secrets
  namespace: tests
stringData:
  GITHUB_TOKEN: <>
  GITHUB_AUTH_PROVIDER_CLIENT_ID: <>
  GITHUB_AUTH_PROVIDER_CLIENT_SECRET: <>
```

Create the `backstage` namespace and apply the Secret you have just defined.

```shell
kubectl create namespace backstage
kubectl apply -f developer-portal-secrets.yml
```
