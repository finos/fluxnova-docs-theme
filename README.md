[![FINOS - Incubating](https://cdn.jsdelivr.net/gh/finos/contrib-toolbox@master/images/badge-incubating.svg)](https://community.finos.org/docs/governance/Software-Projects/stages/incubating)

# Flowave Docs Theme

This repo contains theme elemets for the https://github.com/finos/flowave-docs-manual repository.

## Install

Clone this repository/branch aside of the `flowave-docs-manual`:

```sh
# from the flowave-docs-manual directory
cd ..
git clone git@github.com:flowave/flowave-docs-theme.git
# go into its directory
cd flowave-docs-theme
npm i
npm run build
```

_Note:_ you can clone this repository anywhere,
but you may then change the `setup.target` value of `package.json`.

## Working

After installing (you probably want to have [hugo running as watching server][building-docs])
and then run `npm run build` from this directory.

## Consuming the theme

1. Edit the `setup.target` value of `package.json` to point to the theme's root directory in your Hugo project (default: `../flowave-docs-manual/themes/flowave`).
2. Build and update the theme in the target location by either running:
   1. `grunt build` for building and syncing non-minified assets
   2. Run additionally `grunt optimize` for building and syncing minified assets  

### Using git subtree

You can also consume the theme in a project via git subtree:

Adding the latest version of the theme as `flowave`:

```bash
git subtree add -P themes/flowave git@github.com:flowave/flowave-docs-theme.git dist --squash
```

Updating the theme to the latest version:

```bash
git subtree pull -P themes/flowave git@github.com:flowave/flowave-docs-theme.git dist --squash
```

### Theme development with Virtualbox

This would be the command to execute in order to make the local development site
of `flowave-docs-manual` (see `--baseUrl` option) available in a virtualbox (typically for IE).
Livereload should be deactivate (see `--disableLiveReload`) if you want to develop for IE9.

```sh
hugo --bind="0.0.0.0" --baseUrl="http://10.0.2.2:1313/manual/develop/" -w --disableLiveReload=true server
```

The development site is then available on `http://10.0.2.2:1313/manual/develop/` in your virtualbox
guest OS.

## Contributing
For any questions, bugs or feature requests please open an [issue](https://github.com/finos/flowave-docs-theme/issues)
For anything else please send an email to help@finos.org.

To submit a contribution:
1. Fork it (<https://github.com/finos/flowave-docs-theme/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Read our [contribution guidelines](.github/CONTRIBUTING.md) and [Community Code of Conduct](https://www.finos.org/code-of-conduct)
4. Commit your changes (`git commit -am 'Add some fooBar'`)
5. Push to the branch (`git push origin feature/fooBar`)
6. Create a new Pull Request

_NOTE:_ Commits and pull requests to FINOS repositories will only be accepted from those contributors with an active, executed Individual Contributor License Agreement (ICLA) with FINOS OR who are covered under an existing and active Corporate Contribution License Agreement (CCLA) executed with FINOS. Commits from individuals not covered under an ICLA or CCLA will be flagged and blocked by the FINOS Clabot tool (or [EasyCLA](https://community.finos.org/docs/governance/Software-Projects/easycla)). Please note that some CCLAs require individuals/employees to be explicitly named on the CCLA.

*Need an ICLA? Unsure if you are covered under an existing CCLA? Email [help@finos.org](mailto:help@finos.org)*

## License

Copyright 2025 FINOS

Distributed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

SPDX-License-Identifier: [Apache-2.0](https://spdx.org/licenses/Apache-2.0)
