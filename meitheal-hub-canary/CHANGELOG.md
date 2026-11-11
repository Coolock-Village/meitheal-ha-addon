# Changelog — Meitheal Canary

Canary versions identify a source commit. Images are promoted after release checks and the Home Assistant Green workload pass.

## b2e25f8c5cf5

- Prepare the Home Assistant integration credential before updating. Turn off automatic updates on older installations until that migration is complete; this version is marked as a breaking change.
- Backups stop the App before archiving SQLite. The App no longer mounts Home Assistant configuration or requests the unused authentication API grant. Loki forwarding starts only when configured.

Use the public source build with board keyboard navigation and task actions. This update continues through the existing Meitheal Canary image family.

Home Assistant API access requires verified ingress or a scoped API token. Update and configure the native Meitheal integration before switching an older installation. See the [authenticated integration setup](https://github.com/ryan-winkler/meitheal/tree/7c55683541c237d0c70090ae7ee9a74bb9b2179e/integrations/home-assistant).

For source changes, see the [public project](https://github.com/ryan-winkler/meitheal/commit/b2e25f8c5cf54a174f65e9f95c510ff92144eddc).
