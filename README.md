# @eclass/semantic-release-npm-github-config

[![npm version](https://img.shields.io/npm/v/@eclass/semantic-release-npm-github-config.svg)](https://www.npmjs.com/package/@eclass/semantic-release-npm-github-config)
[![npm downloads](https://img.shields.io/npm/dm/@eclass/semantic-release-npm-github-config.svg)](https://www.npmjs.com/package/@eclass/semantic-release-npm-github-config)
![Node.js CI](https://github.com/eclass/semantic-release-npm-github-config/workflows/Node.js%20CI/badge.svg)
[![Maintainability](https://api.codeclimate.com/v1/badges/ac3f78a532b19f7ee027/maintainability)](https://codeclimate.com/github/eclass/semantic-release-npm-github-config/maintainability)
![Libraries.io dependency status for latest release](https://img.shields.io/librariesio/release/npm/@eclass/semantic-release-npm-github-config)

> [Semantic-release](https://github.com/semantic-release/semantic-release) shareable config for [NPM](https://www.npmjs.com/) with [GitHub](https://github.com/).

## Usage

### Local installation

```bash
npm i -D semantic-release @eclass/semantic-release-npm-github-config @semantic-release/{changelog,git}
```

In `package.json`:

```json
{
  "release": {
    "extends": "@eclass/semantic-release-npm-github-config"
  }
}
```

### Global installation

```bash
$ npm i -g semantic-release @eclass/semantic-release-npm-github-config @semantic-release/{changelog,git}
$ semantic-release -e @eclass/semantic-release-npm-github-config
```

## Configuration

### GitHub authentication

The GitHub authentication configuration is **required** and can be set via [environment variables](#environment-variables).

See [GitHub authentication](https://github.com/semantic-release/gitlab#gitlab-authentication).

### Npm registry authentication

The npm authentication configuration is **required** and can be set via [environment variables](#environment-variables).

See [Npm registry authentication](https://github.com/semantic-release/npm#npm-registry-authentication)

### Environment variables

| Variable                     | Description                                                                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `GH_TOKEN` or `GITHUB_TOKEN` | **Required.** The token used to authenticate with GitLab repository.                                                                        |
| `NPM_TOKEN`                  | **Required.** Npm token created via [npm token create](https://docs.npmjs.com/getting-started/working_with_tokens#how-to-create-new-tokens) |

### Additional options

This shareable config uses the [`@semantic-release/changelog`](https://github.com/semantic-release/changelog), [`@semantic-release/git`](https://github.com/semantic-release/git), [`@semantic-release/github`](https://github.com/semantic-release/github) and [`@semantic-release/npm`](https://github.com/semantic-release/npm) plugins. See the documentation of each plugins for additional options.
Options can be set in the Semantic-release configuration.

For example to set a custom GitHub URL:

```json
{
  "release": {
    "extends": "@eclass/semantic-release-npm-github-config",
    "githubUrl": "https://custom.github.com"
  }
}
```

## License

[MIT](https://tldrlegal.com/license/mit-license)
