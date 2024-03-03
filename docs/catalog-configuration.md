# Catalog Configuration

You can provide a static configuration to populate the Software Catalog by providing one or more locations in the installation `values.yml` file.

```yaml
backstage:
  appConfig:
    catalog:
      locations:
        - type: url
          target: https://github.com/ThomasVitale/symphony-for-dev-and-platform/blob/main/platform/catalog/organization/catalog-info.yml
          rules:
            - allow: [User, Group, Location]
        - type: url
          target: https://github.com/ThomasVitale/symphony-for-dev-and-platform/blob/main/platform/catalog/templates/catalog-info.yml
          rules:
            - allow: [Template, Location]
```
