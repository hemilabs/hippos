# HIPPO001

## Summary

```
HIPPO: 1
Title: HIPPO Purpose and Guidelines
Author: John C. Vernaleo  <jcv@hemi.xyz>
Comments-Summary: No comments yet.
Comments-URI: NA
Status: New
Type: Process
Created: 2025-10-14
Superseded-By: NA
```

## What is a HIPPO

HIPPO is a Hemi Improvement ProPOsal.  These are design documents to
describe changes to the Hemi Network.

## HIPPO Process

All major changes and updates to the Hemi Network should have an
accompanying HIPPO that describes the change, the steps needed for
infrastructure runners, and any user-visible changes.

HIPPOs should be submitted BEFORE a change goes live.

HIPPOs are numbered in the order they are received in this repository.
The order in no way indicated the order or status of the actual
changes.  The status field of the HIPPO is what determines if it has
actually been deployed.

Outside of status updates and minor changes (typos, cosmetic, etc.),
HIPPOs should not be changed once made active.  They should always be
superseded by another HIPPO in the case that a significant change is
needed.

## HIPPO Types

The following types of HIPPOs are prossible:

* Process: These describe some change in the way updates to the Hemi
  Network or the HIPPO process itself work.
* Network: These describe some change to the Hemi Network itself.
  This can range from a major change to the daemon that run Hemi to
  follow a new Ethereum hardfork.
* Misc: These are proposals that do not cleanly fall into one of the
  other categories.

## HIPPO Work Flow

All HIPPOS must be submitted to this
[repository](https://github.com/hemilabs/hippos) as pull requests.
They must be in Markdown and should follow the format of this file and
MUST include a summary section containing:

```
HIPPO:
Title:
Author:
Comments-Summary:
Comments-URI:
Status:
Type:
Created:
Superseded-By:
```

When initially submitted, the status should be `New`.

Once active or in use, the status should be changed to `Active`.

If a new HIPPO replaces it, it should be changed to `Replaced`.

A HIPPO that is no longer being considered should be changed to
`Withdrawn` or `Rejected`.

A HIPPO that is not yet ready for full consideration can be listed as
`Draft`.

## History

This document was heavily influenced by bip-0001.

## Changelog

2025-10-14 Initial version.

