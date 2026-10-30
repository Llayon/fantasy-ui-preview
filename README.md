# Fantasy UI preview

[Open the mobile U2 prototype](https://llayon.github.io/fantasy-ui-preview/heroes-stand.html)

Standalone Fantasy UX U2, roster v8.2: five factions, 40 troop types, 15 heroes,
army preparation, camera and replay. Training is calculated in the browser.
Other menu scenarios are explicitly labelled fixtures. No accounts, cloud or
backend are connected. Browser storage belongs only to this prototype.

This repository contains only the Pages workflow and this description.
Reviewed static builds are release assets, never generated bundle commits.
The private Fantasy source repository and production deployment are separate.

To publish an already uploaded release from the permitted main branch:

```sh
gh workflow run deploy.yml --repo Llayon/fantasy-ui-preview --ref main -f release_tag=u2-v8.2-20261030
```

The workflow checks SHA256 and every static file in the manifest, then deploys
the artifact with the official GitHub Pages actions. It uses only the
repository's ephemeral GITHUB_TOKEN and does not rebuild the game or require
production credentials.
