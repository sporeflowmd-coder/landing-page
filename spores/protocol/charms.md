---
Description: Charm spores are plugins that customize the behaviour of SporeFlow, adding specific capabilities to suit different development needs.
Status: mature
---
# Charms: The Mycelial Plugins

## 🎯 Goal
Define Charms as plugins that customize the behaviour of SporeFlow, providing specialized capabilities for different aspects of code manifestation and deployment.

## 🌿 What are Charms?
Charms are like plugins that customize the behaviour of SporeFlow. They are specialized tools that can be enabled to modify how the mycelium manifests code, adding specific capabilities to suit different development needs. The charm system is extensible, allowing new capabilities to be added as needed.

## 🔧 Built-in Charms

### Tracing Charm
Adds easier code debugging and editing capabilities through strategic comments and breadcrumbs. This helps developers understand how code was manifested and trace back to the original intent.

### Substrate Charm
Manages secrets and environment variables rules, ensuring sensitive data stays isolated in the protected substrate path. This charm enforces the separation between public and private configuration.

### Build Charm
Defines rules about how to deploy manifested code, controlling the output structure, bundling options, and deployment targets.

### Future Charms
The charm system is designed to be extensible. New charms can be created to add capabilities for testing, documentation generation, performance optimization, and more.

## 📥 Input Dependencies
- `spores/manifest.md` (For understanding the protocol vision)
- `spores/_shadow/architecture.md` (For technical constraints)
- `spores/_food/substrate.md` (For understanding secret management)

## 📤 Output Dependencies
- `/root/` (Charms documentation in manifested biomass)
