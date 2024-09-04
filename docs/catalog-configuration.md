# Catalog Configuration

You can provide a static configuration to populate the Software Catalog by providing one or more locations in the installation `values.yml` file.

```yaml
backstage:
  appConfig:
    catalog:
      locations:
        - type: url
          target: https://github.com/kadras-io/kadras-developer-portal/blob/main/demo-catalog/organizations/organization-kadras.yml
          rules:
            - allow: [User, Group, Location]
        - type: url
          target: https://github.com/kadras-io/kadras-developer-portal/blob/main/demo-catalog/templates/templates.yml
          rules:
            - allow: [Template, Location]
```
