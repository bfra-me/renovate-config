# bfra-me/renovate-config

<div align='center'>

[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/bfra-me/renovate-config?sort=semver&style=for-the-badge&logo=github&label=release)][release] [![GitHub Workflow CI Status](https://img.shields.io/github/actions/workflow/status/bfra-me/renovate-config/ci.yaml?branch=main&style=for-the-badge&logo=github%20actions&logoColor=white&label=ci)][ci-workflow]

</div>

[release]: https://github.com/bfra-me/renovate-config/releases 'GitHub release'
[ci-workflow]: https://github.com/bfra-me/renovate-config/actions?query=workflow%3Aci 'Search GitHub Actions for CI workflow runs'

This repository contains [Renovate](https://renovatebot.com/) configuration presets used by [bfra.me](https://bfra.me) projects. It also hosts a reusable [GitHub Actions workflow](.github/workflows/renovate.yaml) that runs Renovate on a schedule.

## Usage

```json
{
  "extends": ["github>bfra-me/renovate-config#5.0.1"]
}
```

## License

[MIT](LICENSE.md)
