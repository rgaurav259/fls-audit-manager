# Changelog — FLS Audit Manager for Salesforce

All notable changes to this project are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [1.0.0] — 2026-04-06

### Initial Release

#### Core Features
- Detect missing Field-Level Security for any Salesforce object across all profiles
- Support for all field types: Text, Email, Checkbox, Picklist, Multi-Select Picklist,
  Date, DateTime, Currency, Number, Percent, Phone, URL, Lookup, Long Text Area,
  Rich Text Area, Time, Formula (read-only shown correctly)
- Tooling API field discovery — correctly detects fields even when current user
  has no FLS (fixes false "no fields found" on custom objects)

#### Audit Features
- Real-time audit with progress bar and status messages
- "Missing Only" and "All Fields" view modes
- Field search with instant filtering
- Profile search and quick-select (All / None / Custom / Standard)
- Stats panel: Total Fields, With FLS, Missing FLS, Total Entries

#### Fix Features
- Single cell click to cycle FLS (Missing → Full → Read Only → Revoke)
- Row-level "Grant All" button with loading state
- Bulk "Fix All Missing" — grants Read+Edit for all missing entries at once
- Bulk "Revoke All FLS" — removes all FLS records for selected profiles
- sObject Collections API (200 records per batch) — handles large orgs efficiently
- Partial success handling — continues if some profiles are license-restricted

#### Export
- CSV export with full audit data: field names, types, per-profile read/edit status

#### UX
- Confirmation modal for bulk operations (replaces browser confirm())
- Meaningful progress messages during bulk operations
- Human-readable error titles (Session Expired, Network Error, Timeout, etc.)
- Toast notifications for all operations
- Org type detection (Production / Sandbox / Developer / Scratch)

#### Technical
- Manifest V3 compliant — zero inline handlers
- Session extraction with 8 fallback methods
- Session validation before use — no stale session errors
- 3-minute timeout on all long-running operations
- Object list: Standard objects first, then Custom objects, both alphabetical
- Profile header/data column alignment fix
- Type pill truncation for long Lookup field lists

#### Exclusions (fields never flagged as missing)
- System audit fields: Id, CreatedDate, LastModifiedDate, SystemModstamp, etc.
- Data.com fields: CleanStatus, CompanyDunsNumber, DandbCompanyId (read-only by Salesforce)
- Address compound sub-fields
- Geocoding suffix fields
