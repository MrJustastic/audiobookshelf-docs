---
id: security
sidebar_label: Security Reports
title: Security Reports
sidebar_position: 10
---

Security issues should be privately disclosed using GitHub's vulnerability reporter in the respective repository. You can also reach out directly through e-mail or Discord to disclose a vulnerability if you are unable to use GitHub. Do not post the vulnerabilities in a public channel on Discord.

Security vulnerabilities with the server should be reported [here](https://github.com/advplyr/audiobookshelf/security).

Security vulnerabilities with the mobile apps should be reported [here](https://github.com/advplyr/audiobookshelf-app/security).

It may take some time to review and respond to vulnerabilities due to an increasing number of reports with the increased usage of AI tools.

## Common False Positives

The following should not be reported as a vulnerability.

### No authentication on image retrieval

By design, there is no authentication to retrieve images from the Audiobookshelf server. This [greatly improves server performance](https://github.com/advplyr/audiobookshelf/discussions/3570). Author and Cover images must be retrieved by UUID, which is randomly generated and not based on the name of the item.

Audio files are accessible without authentication when using an open session.

If other media files are accessible without authentication, that should still be reported.

### Vue2 web client is EOL

The web client was built on Vue 2 and Nuxt 2, both of which have been EOL since 2023. The web client is currently being rewritten and [migrated to React](https://github.com/audiobookshelf/audiobookshelf-client-react). There is no need to report the framework and associated packages are old.

### Outdated libraries

There are a number of old libraries related to the EOL Vue2 web client. There is no need to report these packages as out of date.

### Outdated E-Reader

The EOL Vue2 web client uses old libraries for MOBI (https://kdp.amazon.com/en_US/help/topic/GULSQMHU5MNH4EZM) and AZW3 (https://en.wikipedia.org/wiki/Kindle_File_Format), which Amazon no longer supports. The software libraries for Audiobookshelf have already been updated in the new React client.
