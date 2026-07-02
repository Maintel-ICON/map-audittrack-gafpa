# Project Overview

There are two parts to this project, hosted as a static site via **GitHub Pages** from this `docs` folder.

1. **The installation wizard** (`wizard/`) — the URL set in the Genesys Client App / Premium App integration configuration. It authenticates the installing admin, checks the AuditTrack product is enabled, provisions the access role, and marks the integration installed.

2. **The Premium App landing (holding) page** (`index.html`) — where the wizard redirects after installation, or immediately if it determines the app is already installed. This is the page users see inside Genesys Cloud, with links to help, FAQ, sales, and support.
