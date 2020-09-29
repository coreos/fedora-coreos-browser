# Browsers for Fedora CoreOS releases

This repository contains the source for several standalone HTML pages, which are used by developers in order to more easily browse Fedora CoreOS (FCOS) releases.

 * [browser for FCOS releases](./browser) ([hosted](https://builds.coreos.fedoraproject.org/browser))
 * [browser for FCOS update graph](./graph) ([hosted](https://builds.coreos.fedoraproject.org/graph))

## Deploying

Right now, it's a manual process. E.g.:

```sh
aws s3 cp --profile fcos-builds-mgmt --acl=public-read \
    browser/index.html s3://fcos-builds/browser \
    --cache-control max-age=60
```

We might merge this repo into
[fedora-coreos-streams](https://github.com/coreos/fedora-coreos-streams)
eventually which already has auto-syncing in place.
