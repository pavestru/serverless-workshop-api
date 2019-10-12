# Serverless Node.js Starter

This repository was scaffolded using 

``` bash
$ serverless install --url https://github.com/AnomalyInnovations/serverless-nodejs-starter --name my-project
```

### Requirements

- [Install the Serverless Framework](https://serverless.com/framework/docs/providers/aws/guide/installation/)
- [Configure your AWS CLI](https://serverless.com/framework/docs/providers/aws/guide/credentials/)

### Installation

Install the Node.js packages

``` bash
$ npm install
```

### Usage

To run a function on your local

``` bash
$ serverless invoke local --function hello
```

To simulate API Gateway locally using [serverless-offline](https://github.com/dherault/serverless-offline)

``` bash
$ serverless offline start
```

Deploy your project

``` bash
$ serverless deploy
```

Deploy a single function

``` bash
$ serverless deploy function --function hello
```

#### Running Tests

Run your tests using

``` bash
$ npm test
```

We use Jest to run our tests. You can read more about setting up your tests [here](https://facebook.github.io/jest/docs/en/getting-started.html#content).

#### Environment Variables

To add environment variables to your project

1. Rename `env.example` to `.env`.
2. Add environment variables for your local stage to `.env`.
3. Uncomment `environment:` block in the `serverless.yml` and reference the environment variable as `${env:MY_ENV_VAR}`. Where `MY_ENV_VAR` is added to your `.env` file.
4. Make sure to not commit your `.env`.

#### Linting

We use [ESLint](https://eslint.org) to lint your code via the [serverless-bundle](https://github.com/AnomalyInnovations/serverless-bundle) plugin.

You can turn this off by adding the following to your `serverless.yml`.

``` yaml
custom:
  bundle:
    linting: false
```

To [override the default config](https://eslint.org/docs/user-guide/configuring), add a `.eslintrc.json` file. To ignore ESLint for specific files, add it to a `.eslintignore` file.

### Support

- Open a [new issue](https://github.com/AnomalyInnovations/serverless-nodejs-starter/issues/new) if you've found a bug or have some suggestions.
- Or submit a pull request!

---

This repo is maintained by [Anomaly Innovations](https://anoma.ly); makers of [Seed](https://seed.run) and [Serverless Stack](https://serverless-stack.com).
