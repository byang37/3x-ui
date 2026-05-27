# 3X-UI Fork: Traffic Multiplier

This repository is a personal fork of 3X-UI. It follows the upstream project and keeps fork-specific documentation focused on the features added outside the upstream codebase.

## Main Added Feature

### Inbound Traffic Multiplier

This fork adds a traffic multiplier for inbound nodes.

- The Add Inbound and Edit Inbound forms include a Traffic Multiplier input.
- The default multiplier is `1`, which keeps the original upstream traffic behavior.
- When the multiplier is set to `2`, inbound upload and download traffic are counted as twice the actual usage.
- Per-client upload and download traffic under an inbound are also counted with the multiplier.
- Client remaining traffic and traffic-limit checks use the weighted traffic values.
- Remote node inbound sync includes the multiplier value.
- Subscription links are not changed. Subscription traffic usage and remaining quota are based on the weighted client counters.

## Install This Fork

```bash
bash <(curl -Ls https://raw.githubusercontent.com/byang37/3x-ui/master/install.sh)
```

## Upstream Reference

This fork is based on the upstream project:

[MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)
