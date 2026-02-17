# Architectus Linux - Claude Instructions

## Overview

Linux spoke for Architectus documentation hub.

## Structure

```
docs/asciidoc/
├── antora.yml           # Component: linux
└── modules/ROOT/
    ├── nav.adoc
    └── pages/
        ├── administration/
        ├── hardening/
        ├── eap-tls/
        ├── networking/
        ├── storage/
        ├── containers/
        ├── automation/
        ├── distributions/
        └── troubleshooting/
```

## Rules

1. **Use attributes** from antora.yml - never hardcode paths, distros, package managers
2. **Multi-distro** - provide tabbed examples for Arch, RHEL, Debian
3. **Verification commands** - always show how to verify before/after changes
4. **No TOC attributes** - UI handles navigation
5. **Cross-references** - use `xref:linux::page.adoc[]` for internal, `xref:security::page.adoc[]` for other spokes

## Key Attributes

- `{distro-arch}`, `{distro-rhel}`, `{distro-debian}`
- `{pkg-arch}`, `{pkg-rhel}`, `{pkg-debian}`
- `{path-etc}`, `{path-ssl-certs}`, `{path-systemd}`
- `{svc-sshd}`, `{svc-networkmanager}`, `{svc-firewalld}`

## Building

```bash
# From hub
cd ~/atelier/_architectus/architectus-docs
make serve
```
