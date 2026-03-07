# 🧠 Immune System (Post-Mortems)
Errors and fixes are recorded here to prevent regressions.

---

## Entry 001: Charms Documentation Inconsistency

**Date:** 2026-03-07

**Issue:** The charms section in the manifested HTML (`/root/src/index.html`) and the charms spore (`/spores/protocol/charms.md`) contained inconsistent and incorrect documentation. The documentation incorrectly explained charms as primarily "code fingerprinting" tools with detailed examples of origin/validation fingerprints, when in fact charms should be described simply as plugins that customize SporeFlow behavior.

**Root Cause:** The previous manifestation confused the "Tracing" charm (which does leave breadcrumbs) with the general concept of charms. This led to describing specific implementation details instead of the high-level plugin concept.

**Fix Applied:**
1. Updated `/root/src/index.html` - Simplified the charms section to describe charms as plugins that customize SporeFlow behavior. Removed detailed code fingerprint examples and replaced with a list of built-in charms (Tracing, Substrate, Build).
2. Updated `/spores/protocol/charms.md` - Rewrote the spore to describe charms as plugins, listing the built-in charms with their purposes.

**Prevention Instructions:** When updating charm documentation, ensure the description emphasizes that charms are plugins for customizing behavior, not code tracing tools specifically. Only the Tracing charm deals with code fingerprints; Substrate handles secrets, Build handles deployment, etc.
