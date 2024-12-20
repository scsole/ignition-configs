# ignition-configs

Ignition configs for Fedora CoreOS instances I am using.

## Butane to Ignition Conversion

Generate an Ignition config using Butane. For example, via a container:

```sh
podman run --interactive --rm quay.io/coreos/butane:release --pretty --strict < config.bu > config.ign
```

Reference: [Producing an Ignition Config](https://docs.fedoraproject.org/en-US/fedora-coreos/producing-ign/)

## Using a Config

```sh
sudo coreos-installer install /dev/nvme0n1 --ignition-url ignition-url
```

| File             | Short Description              | Ignition URL                                                                                |
| ---------------- | ------------------------------ | ------------------------------------------------------------------------------------------- |
| config.bu        | Base config                    | https://raw.githubusercontent.com/scsole/ignition-configs/refs/heads/main/config.ign        |
| un100p-vlan30.bu | Minisforum UN100P with VLAN 30 | https://raw.githubusercontent.com/scsole/ignition-configs/refs/heads/main/un100p-vlan30.ign |

## Device Customization Notes

### Minisforum UN100P

Changes from defaults:

- Advanced
  - Oem Entend Setup Configuration
    - Auto Power On: `Enabled`
- Security
  - Secure Boot
    - Secure Boot Mode: `Custom`
    - Reset To Setup Mode
