# Tailscale Orb for CircleCI
<!---
[![CircleCI Build Status](https://circleci.com/gh/james-crowley/tailscale.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/james-crowley/tailscale) [![CircleCI Orb Version](https://badges.circleci.com/orbs/james-crowley/tailscale.svg)](https://circleci.com/orbs/registry/orb/james-crowley/tailscale) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/james-crowley/tailscale/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

--->

This orb allows a user to install and connect to a Tailscale network. 

## Parameters

| Parameters               | Meaning                                                 | Defaults |
|--------------------------|---------------------------------------------------------|----------|
| tailscale-auth-key       | Auth Key from Tailscale used to connect to a Network    | N/A      |
| tailscale-optional-flags | Any additional flags wanted while issuing tailscale up  | N/A      |


Please note it is recommended to utilize *ephemeral* keys while utilizing this orb. Ephemeral keys are made for CI/CD systems that spin up and down
on a regular basis. Thus the keys will automatically be cleaned up after a short period of inactivity. For more information on ephemeral keys please
refer to Tailscale's docs located [here](https://tailscale.com/kb/1111/ephemeral-nodes/).


## How to Utilize this Orb

Here are some rough steps to get started with this orb:

- Generate an ephemeral key on Tailscale's UI
- Add the ephemeral key to CircleCI's Environment Variable section under Project Settings. Variable name should be called `TAILSCALE_AUTHKEY`
- Add the orb to your `config.yml`
- Call the install command, followed by the start command to connect to your Tailscale network


## How to Contribute

We welcome [issues](https://github.com/james-crowley/tailscale/issues) to and [pull requests](https://github.com/james-crowley/tailscale/pulls) against this repository!
