# Changelog — Meitheal Canary

Canary versions identify a source commit. Images are promoted after release checks and the Home Assistant Green workload pass.

## fec6e08e09f3

- Preserve existing Eisenhower scores when a task read fails.
- Turn off automatic updates and prepare the Home Assistant integration credential before updating. If the old App does not expose **Agent Tokens**, stage the updated integration, update the App, then create the token and reauthenticate or reconfigure the existing entry in the same maintenance window. Verify the integration before restoring your automatic update preference.
- Backups stop the App before archiving SQLite. The App no longer mounts Home Assistant configuration or requests the unused authentication API grant. Loki forwarding starts only when configured.

Use the public source build with board keyboard navigation and task actions. This update continues through the existing Meitheal Canary image family.

Home Assistant API access requires verified ingress or a scoped API token. Update and configure the native Meitheal integration before switching an older installation. See the [authenticated integration setup](https://github.com/ryan-winkler/meitheal/tree/7c55683541c237d0c70090ae7ee9a74bb9b2179e/integrations/home-assistant).

For source changes, see the [public project](https://github.com/ryan-winkler/meitheal/commit/fec6e08e09f315dec31a2c9242b6ef91c6949e10).
