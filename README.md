# apps

Links to apps used at Clinical Genomics.

## Install

You need a working Node.js + npm setup to develop the site. Then all you need is to install the dependencies using:

```bash
# install dependencies
npm install
```

## Develop

The site compiles using Node.js and uses the frontend framework Vue.js.

```bash
# serve with hot reload at localhost:8080
npm run dev
```

## Deploy

```bash
# build for production with minification
npm run build
```

The site is hosted in an Amazon S3 bucket. There's a predefined deployment script under `scripts/deploy` that can be run to update the production site. Before that will work you need to install and authenticate the Amazon AWS command line interface:

```bash
pip install awscli
```
