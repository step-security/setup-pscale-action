[![StepSecurity Maintained Action](https://raw.githubusercontent.com/step-security/maintained-actions-assets/main/assets/maintained-action-banner.png)](https://docs.stepsecurity.io/actions/stepsecurity-maintained-actions)

# PlanetScale CLI for GitHub Actions

Use this Action to install `pscale` on your actions runner. Works with Linux, Mac and Windows runners.

```yaml
- name: Setup pscale
  uses: step-security/setup-pscale-action@v1
- name: Use pscale
  env:
    PLANETSCALE_SERVICE_TOKEN_ID: ${{ secrets.PLANETSCALE_SERVICE_TOKEN_ID }}
    PLANETSCALE_SERVICE_TOKEN: ${{ secrets.PLANETSCALE_SERVICE_TOKEN }}
  run: |
    pscale deploy-request list my-db --org my-org
```

Be sure to [setup a service token](https://planetscale.com/docs/concepts/service-tokens) with the proper permissions and add it to your repositories secrets.

**Example with version pinned:**

```yaml
- name: Setup pscale
  uses: step-security/setup-pscale-action@v1
  with:
    version: v0.275.0
```

## License

The action is available as open source under the terms of the [Apache 2.0 License](https://opensource.org/license/apache-2-0/).
