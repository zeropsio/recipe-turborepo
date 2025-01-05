# Zerops x Turborepo

A Basic Turborepo setup for a monorepo project of web and docs on Zerops. [Zerops](https://zerops.io) makes deploying and running Turborepo apps, a breeze.

We also have recipes for [Next.js Static](https://github.com/zeropsio/recipe-nextjs-static) and [Next.js Node.js](https://github.com/zeropsio/recipe-nextjs-nodejs).

![turborepo](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-turborepo.svg)

<br/>

## Deploy on Zerops

You can either click the deploy button to deploy directly on Zerops, or manually copy the [import yaml](https://github.com/zeropsio/recipe-turborepo/blob/main/zerops-project-import.yml) to the import dialog in the Zerops app.

[![Deploy on Zerops](https://github.com/zeropsio/recipe-shared-assets/blob/main/deploy-button/green/deploy-button.svg)](https://app.zerops.io/recipe/turborepo)

<br/>

## Recipe features

- Latest version of Next.js 15 with Turbo 2.3.3 running on a load balanced **Zerops Node.js 20** service
- Both Apps (web and docs) are running on the same service, with the ability to scale horizontally and have their own public access urls.

<br/>

## Production vs. Development

This recipe is ready for production as is, and will scale horizontally by adding more containers in case of high traffic surges. If you want to achieve the highest baseline reliability and resiliace, start with at least two containers (add `minContainers: 2` in recipe YAML in the `app` service section, or change the minimum containers in "Automatic Scaling configuration" section of service detail).

<br/>

## Changes made over the default installation

Added `start:docs` and `start:web` scripts to the root `package.json` to easily start the apps.

If you want to modify your existing Turborepo app to efficiently run on Zerops, there are no changes needed in the codebase on top of the standard installation, just add [zerops.yml](https://github.com/zeropsio/recipe-turborepo/blob/main/zerops.yml) to your repository.

<br/>
<br/>

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).