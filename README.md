# Retarus Transactional Email REST APIs
Contains OpenAPI descriptions and documentation for Retarus Transactional Email APIs.

## Directory Structure Explanation

### `/latest/` Directory

#### Purpose
- Contains the current, active versions of all Retarus Cloud Fax APIs.

#### Redocly Integration
- Individual `openapi/` subdirectories are watched by **Redocly** for API documentation generation (see https://developers.retarus.com/).

#### Content
- Each API has its own subdirectory with **OpenAPI 3.x** specifications and (optional) some additional content.

#### Format
- **OpenAPI 3.x only** — no Swagger 2.x files.

---

### `/latest/*/openapi/` Subdirectories

- **Redocly watched:** These specific folders are monitored by Redocly for changes.
- **Build trigger:** Changes to files in these directories trigger API documentation builds.

**Subdirectories:**
- `latest/sending-email-api/openapi/`

---

### `/legacy/` Directory

#### Purpose
- Contains final **Swagger 2.x** specifications for legacy compatibility.

⚠️ **DEPRECATED**  
These files are in legacy maintenance mode and will not receive updates.

#### Redocly Integration
- Not watched by Redocly but available for download.

#### Maintenance
- **NO ACTIVE MAINTENANCE** — Use OpenAPI 3.x specifications in `/latest/` for all new development.

---

### `/versions/` Directory

#### Purpose
- Archives historical versions of REST APIs for reference.

#### Format & Content
- Contains only **OpenAPI 3.x** files and changelogs.

---

### **Changelog**

A single `CHANGELOG.md` file in the root directory contains changes for all APIs, providing a unified change history across the entire Retarus Cloud Fax API suite.

---

## Transactional Email REST APIs Overview

### Sending Fax API
- Handles fax transmission, scheduling, and delivery management.

  - **Current Version:** Located in `latest/sending-email-api/` (**OpenAPI 3.x**)
  - **Legacy Version:** `legacy/sending-email-api-swagger-2x.json` ⚠️ DEPRECATED
  - **Historical Versions:** `versions/sending-email-api/v[version_number]/`

---

## ⚠️ Important: Swagger 2.x Deprecation Notice

Swagger 2.x specifications in the `/legacy/` directory are **DEPRECATED** and in maintenance mode:

- **No updates:** Legacy Swagger 2.x files will not receive any updates, bug fixes, or new features.
- **OpenAPI 3.x only:** All future development will use OpenAPI 3.x format exclusively.
- **Legacy support:** Swagger 2.x files are maintained only for existing integrations that cannot be immediately upgraded.
- **End of life:** Swagger 2.x support will be completely removed in a future release.

---

## Working with This Repository

### Update Workflow

The current workflow for updating documentation is as follows:

- **Source repository:** OpenAPI descriptions are developed and maintained in Bitbucket.
- **Manual upload:** Updated OpenAPI description files are manually uploaded to this GitHub repository under the appropriate `latest/*/openapi/` directories.
- **Documentation updates:** Manual uploads to GitHub automatically trigger documentation updates via Redocly.
