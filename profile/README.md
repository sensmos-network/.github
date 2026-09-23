# Sensmos

An internet observatory built from home nodes. Each node is a few-dollar ESP32 that
measures the network from real homes, gives you private access to your own LAN, and
turns local sensors into live data.

## What a node does

- **Measures the internet home-to-home** — ICMP, TCP, DNS and HTTP between real homes,
  not to a data centre. Results land on a live map.
- **Remote access to your LAN** — SSH and your Home Assistant panel from the phone,
  without VPN or port forwarding, even behind CGNAT. Off by default, private addresses only.
- **Sensors and automation at the edge** — readings become entities, and small scripts
  run on the node itself, no cloud required.
- **LoRa emergency radio** — when the internet goes down, a node with an SX1262 radio
  sends chosen readings over LoRa; any node or gateway that hears them passes them on to you.

## Privacy

The network sees path metrics — latency, jitter, loss, reachability — never the content
of your traffic. A node's public position is blurred by default, and its identity is a
key pair generated on the device.

## Repositories

| Repo | What it is |
|---|---|
| [sensmos-firmware](https://github.com/sensmos-network/sensmos-firmware) | Open firmware for ESP32 nodes, flashed straight from the browser |
| [sensmos-app](https://github.com/sensmos-network/sensmos-app) | Android app: onboarding, wallet, SSH terminal, Home Assistant panel |
| [sensmos-homeassistant](https://github.com/sensmos-network/sensmos-homeassistant) | Home Assistant integration, installable through HACS |
| [sensmos-esphome](https://github.com/sensmos-network/sensmos-esphome) | ESPHome component that publishes any sensor to the live map |
| [sensmos-gateway](https://github.com/sensmos-network/sensmos-gateway) | Lets a LoRaWAN gateway you already run listen for the network |
| [sensmos-store-desktop](https://github.com/sensmos-network/sensmos-store-desktop) | Desktop client for Sensmos Store — encrypted backup on other node owners' disks |
| [sensmos-protocol](https://github.com/sensmos-network/sensmos-protocol) | GALU token and the on-chain reward pool |

[sensmos.com](https://sensmos.com) · [Live map](https://sensmos.com/map/) · [Flash a node](https://sensmos.com/flash/) · [Docs](https://sensmos.com/docs/)
