# Meitheal Canary — Home Assistant Documentation

**Meitheal Canary** (`/meh·hal/`) is the preview channel for Meitheal — letting you test upcoming household task, routine, project, and Home Assistant integration improvements before they are promoted to a tagged Stable release.

Each Canary build identifies its exact source commit SHA and runs inside its own isolated Home Assistant App container (`meitheal_canary`).

## When to Choose Canary vs. Stable

| Channel | App Name | Best For | Update Cadence |
|---|---|---|---|
| **Stable** | **Meitheal** | Everyday household production use | Tagged SemVer releases |
| **Canary** | **Meitheal Canary** | Previewing new features and validating fixes early | Commit-stamped preview builds |

## 1. Install Meitheal Canary

1. In Home Assistant, open **Settings → Apps → Install app** (or **Settings → Add-ons → Add-on Store**).
2. Open the top-right **⋮** menu, select **Repositories**, and add `https://github.com/ryan-winkler/meitheal-ha-addon`.
3. Select **Meitheal Canary**, then select **Install** and **Start**.
4. Enable **Show in sidebar** if you want quick access, then select **Open web UI**.

## 2. Keep Your Data Safe When Updating or Moving Channels

An update to the same installed App keeps its `/data/meitheal.db` database. Changing the repository URL or switching between **Meitheal** and **Meitheal Canary** gives the App a separate data directory — always make a Home Assistant backup that includes Meitheal before replacing an installation.

If you use the separate Meitheal Core integration in **Settings → Devices & Services**, disable automatic updates before updating:

- If your current App already exposes **Agent Tokens** in **Settings → Automation & AI**, follow the [integration credential migration](https://github.com/ryan-winkler/meitheal/blob/fec6e08e09f315dec31a2c9242b6ef91c6949e10/docs/kcs/home-assistant-core-credentials.md) and verify an authenticated native task read before and after updating.
- If upgrading from an older build without **Agent Tokens**, update the Core integration and the App in the same maintenance window, create a dedicated scoped token in the updated App, and reauthenticate or reconfigure the Core entry so `todo.meitheal_tasks` and task actions stay connected.

## 3. Report an Issue

Include the Canary commit version shown on the App **Info** tab, your Home Assistant version, and the steps to reproduce the issue. Remove access tokens and private household data from any logs or screenshots before posting to [GitHub Issues](https://github.com/ryan-winkler/meitheal-ha-addon/issues).
