# Node.js 18+ binaries for CentOS 7

The official Node.js Linux x64 binaries don't support CentOS 7 and earlier; they now depend on a more recent glibc.

More details here: https://github.com/nodejs/node/issues/43246

We can successfully compile on CentOS 7 from source.

This repository semi-automates these builds using GitHub Actions, and publishes the resulting binaries as attachments to [releases](https://github.com/jcheng5/node-centos7/releases).

As currently written, new builds are created by editing the `NODE_VERSION` value in `.github/workflows/ci.yml`, and pushing that change to the `main` branch. If a release of that version doesn't already exist, then a build and publish will be attempted. (In the future, it would be nice if this workflow ran on a scheduled basis and just built whatever new Node.js it found.)
