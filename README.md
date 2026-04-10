# Puppet Control Repository

This is the main Puppet control repository for the production environment.

## Structure

```
puppet-overall-code/
├── Puppetfile           # Module dependencies (includes xshield_spark)
├── environment.conf     # Environment configuration
├── hiera.yaml          # Hiera 5 configuration
├── data/               # Hiera data
│   └── common.yaml
├── manifests/          # Main manifests
│   └── site.pp
└── site-modules/       # Customer-specific modules
```

## XShield Spark Module

The xshield_spark module is referenced from a separate repository:
- Repository: https://github.com/RajeshKumarCT/puppet-ct-spark
- Branch: rajesh-testing

This separation allows ColorTokens to update the Spark module independently.

## Foreman Integration

Host-to-class assignments are managed via Foreman API, not Hiera.
