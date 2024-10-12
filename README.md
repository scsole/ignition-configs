# ignition-configs

Ignition configs for Fedora CoreOS instances I am using

## Butane to Ignition conversion

Generate an Ignition config using Butane. For example, via a container:

```sh
podman run --interactive --rm quay.io/coreos/butane:release --pretty --strict < config.bu > config.ign
```

Reference: [Producing an Ignition Config](https://docs.fedoraproject.org/en-US/fedora-coreos/producing-ign/)
