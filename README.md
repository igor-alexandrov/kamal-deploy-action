# Kamal Deploy Action

This GitHub Action deploys using Kamal

## Inputs

- **environment**: The environment to deploy to.
- **kamal-registry-username**: Registry username (Digital Ocean access token).
- **kamal-registry-password**: Registry password (Digital Ocean access token).

## Usage

```yaml
steps:
  - name: Kamal Deploy
    uses: your-username/kamal-deploy-action@v1
    with:
      environment: 'staging'
      kamal-registry-username: ${{ secrets.KAMAL_REGISTRY_USERNAME }}
      kamal-registry-password: ${{ secrets.KAMAL_REGISTRY_PASSWORD }}
    # Optional
    env:
      DATABASE_URL: ${{ secrets.DATABASE_URL }}
      REDIS_URL: ${{ secrets.REDIS_URL }}
      RAILS_MASTER_KEY: ${{ secrets.RAILS_MASTER_KEY }}