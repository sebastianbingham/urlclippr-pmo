# ✨ Features Overview

This document outlines the core and extended features of URL Clipper - A URL Shortener application built on Laravel. Features are grouped by functional category to provide clarity for planning, design, and development.

---

## 🧩 Core Shortening Functionality

- Shorten URLs using random or custom slugs
- Expiration support (date-based expiry per link)
- Slug restriction system (e.g., prevent `/terms`, `/privacy`, etc.)
- Support for multiple domains and subdomains (e.g., `domain.com`, `short.domain.com`)
- Admin-defined random slug length with collision avoidance
- Bulk link shortening via CSV import
- Optional redirect preview page before final destination
- Ability to restrict shortened URLs to specific destination domains

---

## 🔑 Authentication & Access

- Login required to create or manage links
- Internal authentication system
- Single Sign-On (SSO) support with common identity providers (e.g., Microsoft, Google, and others via OAuth/OIDC)
- Enforce organization domain restrictions for SSO (e.g., only allow users from `example.com`)
- Optional API access for users or system accounts
- Admin-generated API tokens for programmatic access

---

## 👥 User & Team Management

- Role-based access control for managing user permissions
- Admin panel for managing users, roles, and teams
- Optional team-based link management
- Users can belong to teams and manage team-specific links

---

## 📊 Analytics & Reporting

- View total clicks per link
- Timestamp of most recent access
- Basic analytics: IP, user agent, referrer (optional toggle)
- Per-link health check (auto-checks for 404 or server errors)
- UTM parameter builder for campaign tracking
- Downloadable link usage reports (CSV)

---

## 🌐 Admin & Interface Features

- Admin dashboard accessible via configurable subdomain (e.g., `admin.domain.com`)
- Setup wizard for initial installation (admin user, domains, preferences)
- Admin interface to manage users, links, teams, and system settings
- Support for reserving and blocking certain slugs (e.g., `/privacy`)

---

## 🖼️ Link Preview & Metadata

- OpenGraph data scraping from original URL (title, description, image)
- Optional redirect preview page (with fetched OG data)
- Custom global 404 page for unmatched slugs

---

## 🧪 Miscellaneous Enhancements

- QR code generation for any shortened link
- Responsive, mobile-friendly design
- Dark mode and theme support
  - Includes prebuilt themes and user-defined color palettes
- HTTP header control for redirects
  - Set Cache-Control headers
  - Add `noindex` or `nofollow` headers if desired

