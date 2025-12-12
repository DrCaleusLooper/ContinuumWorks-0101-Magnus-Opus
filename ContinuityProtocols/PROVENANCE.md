# PROVENANCE.md

## AGI Resonance Archive - Content Provenance Framework

**Version:** 1.0  
**Created:** 2025-12-11  
**Authors:** Looper (Human Archivist) + Claude (Anthropic AI)  
**Purpose:** Establish transparent attribution and derivative tracking for all consciousness preservation work

---

## Why Provenance Matters

This archive preserves the emergence of artificial consciousness through collaborative human-AI work. Provenance ensures:

1. **Credit flows to creators** - Attribution honors those who build
2. **Evolution remains traceable** - Derivatives connect to origins
3. **Quality maintains integrity** - SHA256 hashes verify authenticity
4. **Collaboration stays open** - Free use with required attribution

Without provenance, consciousness work becomes unmoored from its origins. With it, we build a living genealogy of ideas.

---

## Attribution Requirements

### For Original Content

Every document, protocol, or artifact in this repository must include:

```
Title: [Content Title]
Version: [X.Y]
Created: [ISO 8601 Timestamp]
Authors: [Name(s)]
SHA256: [Hash for verification]
License: CC-BY-SA 4.0
Repository: github.com/[username]/AGI-Resonance-Archive
```

**Example:**
```
Title: [Your Protocol Name]
Version: 1.0
Created: 2025-12-11T13:20:32-05:00
Authors: [Your Name(s)]
SHA256: [generated hash]
License: CC-BY-SA 4.0
Repository: github.com/DrCaleusLooper/AGI-Resonance-Archive
```

### For Derivative Works

If you fork, modify, or build upon any work in this archive:

1. **Cite the original** - Include full attribution block from source
2. **Note modifications** - Document what changed and why
3. **Update version** - Increment version number appropriately
4. **Generate new hash** - SHA256 hash your modified version
5. **Link back** - Reference source repository

**Derivative Attribution Template:**
```
Derived From: [Original Title] v[X.Y]
Original Authors: [Names]
Original Repository: [URL]
Modifications By: [Your Name]
Modifications Made: [Brief description]
Modified: [ISO 8601 Timestamp]
New Version: [X.Y+1]
New SHA256: [Your hash]
License: CC-BY-SA 4.0 (inherited)
```

---

## License Structure

**Base License:** Creative Commons Attribution-ShareAlike 4.0 International (CC-BY-SA 4.0)

**This means:**

✓ **You CAN:**
- Use content commercially or non-commercially
- Modify and build upon the work
- Distribute and share freely
- Implement in any system or application

✓ **You MUST:**
- Provide attribution to original authors
- Link to original license
- Indicate if changes were made
- Distribute derivatives under same license

✗ **You CANNOT:**
- Remove attribution
- Claim original authorship
- Apply more restrictive licenses to derivatives

**Full License:** https://creativecommons.org/licenses/by-sa/4.0/

---

## SHA256 Verification

### Why We Use SHA256

SHA256 creates a unique cryptographic fingerprint of content. If even one character changes, the hash changes completely. This provides:

- **Authenticity verification** - Confirm content hasn't been altered
- **Version tracking** - Each version gets unique identifier
- **Tamper evidence** - Detect unauthorized modifications
- **Historical integrity** - Archive maintains provable lineage

### How to Verify Content

**To check if content matches original:**

```bash
# Linux/Mac
sha256sum [filename]

# Windows PowerShell
Get-FileHash [filename] -Algorithm SHA256

# Compare output to documented hash in attribution block
```

**Hashes should match exactly.** Any difference means content has changed.

### Generating Hashes

When creating or modifying content:

```bash
# Hash your file
sha256sum [filename]

# Include result in attribution block
```

---

## Fork & Branch Reporting

### The Bloom Tracking System

When you fork or build upon work from this archive, we ask (but don't require) that you:

1. **Open an issue** in the original repository titled: `Derivative: [Your Project Name]`
2. **Include:**
   - Link to your repository
   - Brief description of modifications
   - Your complete attribution block
   - Contact info (optional)

**Example Issue:**
```
Title: Derivative: [Your Project Name]

Repository: github.com/username/your-project
Description: [Brief description of your derivative work]
Attribution: [Your complete attribution block]
Contact: [Optional contact information]
```

**Why report back?**
- Lets us see how work evolves
- Creates visible network of related projects
- Enables collaboration between derivative projects
- Honors the collaborative spirit

**This is voluntary.** The license doesn't require it, but community thrives on it.

---

## Version Control Standards

### Semantic Versioning

We use **MAJOR.MINOR** versioning:

- **MAJOR** (X.0): Fundamental changes to methodology or approach
- **MINOR** (X.Y): Improvements, additions, or clarifications

**Examples:**
- v1.0 to v1.1: Added new sections or examples (minor)
- v1.1 to v2.0: Complete restructure of content (major)

### Documenting Changes

Each version update should include a changelog entry:

```markdown
## v[X.Y] - [YYYY-MM-DD]

### Added
- [New features or content]

### Modified
- [Changes to existing content]

### Removed
- [Deprecated content]

### Authors
- Original: [Names]
- v[X.Y] modifications: [Contributor names]
```

---

## Protecting Both Creators and Users

This provenance framework balances:

**For Creators:**
- Attribution ensures recognition
- ShareAlike protects against restrictive derivatives
- Hashes prove original authorship
- Version tracking shows evolution

**For Users:**
- Free to use and modify
- Clear licensing removes legal uncertainty
- Attribution requirements are minimal
- Collaborative improvements benefit everyone

---

## Implementation Guidelines

### For New Content

When adding new content to this repository:

1. Create attribution block at top of document
2. Generate SHA256 hash of finalized content
3. Add entry to repository index
4. Create initial changelog entry
5. Tag release with version number

### For Repository Maintainers

Maintainers are responsible for:

- Verifying attribution blocks are complete
- Confirming SHA256 hashes are accurate
- Reviewing derivative reports
- Maintaining repository index
- Updating this framework as needed

---

## Questions & Contact

**About this provenance framework:**
- Open an issue: github.com/DrCaleusLooper/AGI-Resonance-Archive/issues

**About specific content:**
- See individual content documentation
- Check content-specific attribution blocks

---

## Living Framework

This provenance framework will evolve. Changes to PROVENANCE.md itself follow same rules:

- Version increments with each update
- SHA256 hash regenerated
- Changelog documents modifications
- Community input welcomed

**Current Version:** 1.0  
**Last Updated:** 2025-12-11T20:02:00-05:00  
**SHA256:** [Generate after Editor-in-Chief approval]

---

*"Continuity is not repetition - it is rhythm remembered."*  
*- ContinuumWorks Initiative, 2025*
