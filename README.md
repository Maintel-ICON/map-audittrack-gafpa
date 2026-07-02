# Maintel AuditTrack Genesys AppFoundry Integration

This repository contains the static application pages required for the Maintel AuditTrack product listing on the Genesys AppFoundry.

AuditTrack, powered by the Maintel Application Platform (MAP), provides secure, long-term audit log storage and archiving, helping organisations meet regulatory and governance requirements while ensuring easy access to their audit data.

## 📄 Repository Structure

```
/docs
    index.html # Premium App landing (holding) page shown inside Genesys Cloud
    help.html # Help Guide with product details and usage instructions
    faq.html # Frequently Asked Questions
    contactus.html # Sales contact details
    support.html # Support contact details
    style.css # Shared styling for all pages
    app.json # Application metadata
    /wizard # Premium App installation wizard (Genesys AppFoundry standard)
```

The site is hosted using **GitHub Pages** and serves as the publicly accessible integration pages required by Genesys for application listing.

## 🔧 How the Genesys Integration Works

1. The AuditTrack Premium App integration is installed from Genesys Cloud **Admin → Integrations** (during development, via the shared `premium-app-example` integration type; after AppFoundry approval, via the dedicated Maintel AuditTrack integration type created by Genesys).
2. The integration's **Application URL** points at the installation wizard: `https://maintel-icon.github.io/map-audittrack-gafpa/wizard/index.html`
3. The wizard authenticates the admin (OAuth PKCE), verifies the product is enabled in the org, provisions the AuditTrack access role, and then redirects to the landing page (`index.html`), which acts as the holding page inside Genesys Cloud.

### Remaining Configuration

- `docs/wizard/config/config.js` → `clientID` must be set to a **Token Implicit / PKCE Code grant OAuth Client** created in the Maintel Genesys Cloud org, with the wizard URL as an authorized redirect URI.
- After AppFoundry approval, update `premiumAppIntegrationTypeId`, `premiumAppViewPermission`, and the role `entityName` in `config.js` to the Genesys-assigned integration type.
- `enableUninstall` in `config.js` should be set to `false` before production listing.

## 🚀 Access the Live Pages

- **Main Page:** [View AuditTrack App Page](https://maintel-icon.github.io/map-audittrack-gafpa/)
- **Help Guide:** [Help Guide](https://maintel-icon.github.io/map-audittrack-gafpa/help.html)
- **FAQ:** [FAQ](https://maintel-icon.github.io/map-audittrack-gafpa/faq.html)

## 🛡️ About AuditTrack

AuditTrack automatically exports and archives audit logs and metadata from supported contact centre platforms (such as Genesys Cloud) to secure AWS storage. It provides:

- Compliant long-term audit log storage
- Search and filter capabilities
- Secure viewing and export functionality
- SSO via Microsoft Entra (Azure AD)
- Role-based access and access audit logging
- Subscription-based pricing (Per User Per Month)

## 🧩 Maintel Contact

For more information about AuditTrack or Maintel's services:

- 🌐 [maintel.co.uk](https://maintel.co.uk)
- 📧 info@maintel.co.uk
- ☎️ 0344 871 1122

---

Maintel delivers cloud-based contact centre solutions and applications that unify, personalise, and enhance customer experiences.

> Solid solutions for a dynamic world.
