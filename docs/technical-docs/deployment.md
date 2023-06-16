---
description: A guide on how to deploy services to both production and staging.
---

# 🚀 Deployment

## Deploy to staging

To deploy to staging, merge to the `staging-main` branch and push the code. The deployment will go through automatically! You can see the [GitHub staging deployment actions to check](https://github.com/CrowdDotDev/crowd.dev/actions/workflows/staging-deploy-backend.yaml) the status. You will also get a notification in the `deploys-staging` Slack channel once it has gone through.

* Run migrations if needed.
* Update the enviroment variables if needed.

## Deploy to production

The production deploy is done with a [GitHub action](https://github.com/CrowdDotDev/crowd.dev/actions/workflows/production-deploy.yaml).&#x20;. You can simply select which services you want to deploy, and the branch (it should 99% of the time be `main`), and click deploy!

* Run migrations if needed.
* Update the enviroment variables if needed.

## Updating environment variables

Environment variables are kept in the [kube repo](https://github.com/CrowdDotDev/kube-crowd). There is a folder for production, and one for staging. There we have environment variables for frontend and backend.

To push an update to the Kubernetes cluster:
1. Make sure you have an up-to-date version of the Kube repo
2. Make the changes you want, and make sure to commit and push them! Otherwise, they could be overwritten by a colleague.
3. Run the `[production/staging]./update-config-map` script to update the values in the cluster.
4. Re-deploy the necessary services.

## Running migrations

Running database migrations is, for now, not a part of the automated deployment. They need to be run manually. To run migrations:

1. Make sure you are in the appropiate branch. If you are running them on production, this is `main`. For staging, `staging-main`. Make sure the branch is up-to-date.
2. Export the directory where crowd.dev is in your system. For example `export CROWD_CHECKOUT_DIR=/Users/joanreyero/Documents/crowd.dev`.
3. Run the script `./migrate-up.sh` to run the migrations.