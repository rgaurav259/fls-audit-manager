# Changelog — FLS Audit Manager for Salesforce

All notable changes to this project are documented in this file.  
This project follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)  
and adheres to [Semantic Versioning](https://semver.org/).

---

## [Unreleased]

---

## [1.0.0] — 2026-04-06

### Added

#### Core Features
- Detect missing Field-Level Security (FLS) for any Salesforce object across all profiles
- Support for all field types: Text, Email, Checkbox, Picklist, Multi-Select Picklist,
  Date, DateTime, Currency, Number, Percent, Phone, URL, Lookup, Long Text Area,
  Rich Text Area, Time, Formula (read-only handled correctly)
- Tooling API-based field discovery to ensure accurate detection even when the current user lacks FLS access

#### Audit Features
- Real-time audit with progress bar and status updates
- "Missing Only" and "All Fields" view modes
- Instant field search and filtering
- Profile search with quick-select (All / None / Custom / Standard)
- Stats panel: Total Fields, With FLS, Missing FLS, Total Entries

#### Fix Features
- Single-click FLS control (Missing → Full → Read Only → Revoke)
- Row-level "Grant All" action with loading state
- Bulk "Fix All Missing" to grant Read + Edit access
- Bulk "Revoke All FLS" for selected profiles
- sObject Collections API support (200 records per batch) for large org handling
- Partial success handling for restricted profiles

#### Export
- CSV export including field names, types, and per-profile access details

#### User Experience
- Confirmation modal for bulk operations (replaces browser confirm)
- Clear progress messages for long-running tasks
- Human-readable error messages (Session Expired, Network Error, Timeout, etc.)
- Toast notifications for all actions
- Org type detection (Production / Sandbox / Developer / Scratch)

#### Technical
- Manifest V3 compliant (no inline scripts)
- Secure session extraction with multiple fallback methods
- Session validation before execution
- 3-minute timeout handling for long operations
- Optimized object listing (Standard → Custom, alphabetical)
- UI alignment fixes for profile headers and data columns
- Lookup field display optimization (truncation handling)

#### Exclusions
- System audit fields: Id, CreatedDate, LastModifiedDate, SystemModstamp, etc.
- Data.com fields: CleanStatus, CompanyDunsNumber, DandbCompanyId
- Address compound sub-fields
- Geocoding-related fields
