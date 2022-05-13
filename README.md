# CPAN deployment tools

This repository contains tools and CI actions to test CPAN dependency deployments using cpanm, Carmel, Carton and cpm.

## Setup

This assumes you use Carmel, Carton or similar tools locally to manage dependencies, then cache the CPAN-style index and tarballs checked into `vendor/cache` directory.

For this repo, the vendor cache is created locally using Carmel. Carmel allows you to declare dependencies in `cpanfile`, then freeze the versions in `cpanfile.snapshot`. The frozen dependencies can be vendored into `vendor/cache` using `carmel package`. You can achieve the same thing using Carton with `carton bundle` as well.

Installation (deployment) scripts are in the `script` directory. The scripts are coded in a way it can bootstrap the installation a host without any CPAN configuration, using `cpanm` script in `vendor`.

## Actions

Each deployment is tested in GitHub Actions, with build cache enabled for some tools that support it.

## Maintainer

Tatsuhiko Miyagawa
