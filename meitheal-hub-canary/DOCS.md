# Meitheal Canary

Canary receives selected Meitheal builds for testing. Each release identifies its source commit. Check the changelog before updating and keep a current backup of your Meitheal data.

## Install Canary

1. In Home Assistant, go to **Settings → Apps → Install app**.
2. Open the top-right menu, choose **Repositories**, and add `https://github.com/ryan-winkler/meitheal-ha-addon`.
3. Select **Meitheal Canary**, then **Install** and **Start**.

## Keep your data when moving an installation

An update to the same installed App keeps its data. Changing the repository URL or switching channels can give the App a different identity and a separate data directory.

Before replacing an existing installation, make a Home Assistant backup that includes Meitheal and verify you can recover its data and settings. Follow the migration instructions in the release notes if the App identity changes. If you use the separate Meitheal Core integration, verify its connection after the move.

## Report an issue

Include the Canary version, your Home Assistant version, and the steps to reproduce the issue. Remove access tokens and household data from any logs or screenshots. [GitHub Issues](https://github.com/ryan-winkler/meitheal-ha-addon/issues)
