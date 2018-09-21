# npm-github-config

[![npm version](https://img.shields.io/npm/v/npm-github-config.svg)](https://www.npmjs.com/package/npm-github-config)
[![npm downloads](https://img.shields.io/npm/dm/npm-github-config.svg)](https://www.npmjs.com/package/npm-github-config)
[![Build Status](https://img.shields.io/travis/lgaticaq/npm-github-config.svg)](https://travis-ci.org/lgaticaq/npm-github-config)
[![Maintainability](https://api.codeclimate.com/v1/badges/707123360dd51ea1ffaf/maintainability)](https://codeclimate.com/github/lgaticaq/npm-github-config/maintainability)
[![devDependency Status](https://img.shields.io/david/dev/lgaticaq/npm-github-config.svg)](https://david-dm.org/lgaticaq/npm-github-config#info=devDependencies)

> [Semantic-release](https://github.com/semantic-release/semantic-release) shareable config for [NPM](https://www.npmjs.com/) with [GitHub](https://github.com/).

## Usage

### Local installation

```bash
npm i -D semantic-release npm-github-config @semantic-release/{changelog,git,npm}
```

In `package.json`:

```json
{
  "release": {
    "extends": "npm-github-config"  
  }
}
```

### Global installation

```bash
$ npm i -g semantic-release npm-github-config @semantic-release/{changelog,git,npm}
$ semantic-release -e npm-github-config
```

## Configuration

### GitHub authentication

The GitHub authentication configuration is **required** and can be set via [environment variables](#environment-variables).

See [GitHub authentication](https://github.com/semantic-release/gitlab#gitlab-authentication).

### Npm registry authentication

The npm authentication configuration is **required** and can be set via [environment variables](#environment-variables).

See [Npm registry authentication](https://github.com/semantic-release/npm#npm-registry-authentication)

### Environment variables

| Variable                     | Description                                                                                   |
|------------------------------|----------------------------------------------------------------------                         |
| `GH_TOKEN` or `GITHUB_TOKEN` | **Required.** The token used to authenticate with GitLab repository.                          |
| `NPM_TOKEN`                  | **Required.** Npm token created via [npm token create](https://docs.npmjs.com/getting-started/working_with_tokens#how-to-create-new-tokens) |

### Additional options

This shareable config uses the [`@semantic-release/changelog`](https://github.com/semantic-release/changelog), [`@semantic-release/git`](https://github.com/semantic-release/git), [`@semantic-release/github`](https://github.com/semantic-release/github) and [`@semantic-release/npm`](https://github.com/semantic-release/npm) plugins. See the documentation of each plugins for additional options.
Options can be set in the Semantic-release configuration.

For example to set a custom GitHub URL:

```json
{
  "release": {
    "extends": "npm-github-config",
    "githubUrl": "https://custom.github.com"
  }
}
```

## License

[MIT](https://tldrlegal.com/license/mit-license)
