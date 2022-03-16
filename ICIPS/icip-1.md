---
ICIP: 1
title: ICIP Purpose and Guidelines
status: Living
type: Meta
author: John Plevyak <jplevyak@Internet Computer.org>, et al.
created: 2022-03-08
---

## What is an ICIP?

ICIP stands for Internet Computer Improvement Proposal. A ICIP is a document providing information to the Internet Computer community, or describing a process or feature of Internet Computer or in relattion to its environment. The ICIP should provide a concise description, (design if applicable) and rationale. The ICIP author is responsible for building consensus within the community and documenting dissenting opinions.

## ICIP Rationale

We intend ICIPs to be the primary mechanisms for proposing changes, for collecting community input, and for documenting the decisions that go into Internet Computer. Because the ICIPs are maintained as text files in a versioned repository, they are the historical record of Internet Computer policy.

## ICIP Types

There are four types of ICIP:

- An **Informational ICIP** describes a Internet Computer issue, or provides general guidelines or information to the Internet Computer community, but does not propose a new process. Informational ICIPs do not necessarily represent Internet Computer community consensus or a recommendation, so users and implementers are free to ignore Informational ICIPs.

- A **Standard ICIP** describes any change that affects Internet Computer features and processes.

- A **Meta ICIP** describes a process surrounding Internet Computer or proposes a change to such a process. Meta ICIPs are like Standard ICIPs but apply to areas other than Internet Computer proper. They may propose an implementation, but outside of the Internet Computer codebase; they often require community consensus; unlike Informational ICIPs, they are more than recommendations, and users are typically not free to ignore them.

It is highly recommended that a single ICIP contain a single key proposal or new idea.

A ICIP must meet certain minimum criteria. It must be a clear and complete description of the proposed change. The change must represent a net improvement. The proposed implementation, if applicable, must be solid and must not overly complicated.

## ICIP Work Flow

### Shepherding an ICIP

Parties involved in the process are the *ICIP author* and the [*ICIP editors*](#ICIP-editors).

Before you begin writing a formal ICIP, you should discuss your idea on [Discussions](https://github.com/dfinity/ICIPs/discussions).

Once the idea has been vetted, your next responsibility will be to present a ICIP to the reviewers and all interested parties to give feedback.

### ICIP Process 

The following is the standardization process for all ICIPs in all tracks:

**Idea** - This is the state where the idea is presented on [Discussions](https://github.com/dfinity/ICIPs/discussions) before it is a ICIP.

**Draft** - The first formally tracked stage of a ICIP in development. A ICIP is merged by a ICIP Editor into the repository when it has been discussed and properly formatted.

**Review** - A ICIP Author marks a ICIP as ready for and requesting Review.

**Last Call** - This is the final review window for a ICIP before moving to `Final`. A ICIP editor will assign `Last Call` status and set a review end date (`last-call-deadline`), typically 14 days later.

If this period results in necessary normative changes it will revert the ICIP to `Review`.

**Final** - This ICIP represents the final standard. A Final ICIP exists in a state of finality and should only be updated to correct errata and add non-normative clarifications.

**Stagnant** - Any ICIP in `Draft` or `Review` or `Last Call` if inactive for a period of 6 months or greater is moved to `Stagnant`. An ICIP may be resurrected from this state by Authors or ICIP Editors through moving it back to `Draft` or it's earlier status. If not resurrected, a proposal may stay forever in this status. 

**Withdrawn** - The ICIP Author(s) have withdrawn the proposed ICIP. This state has finality and can no longer be resurrected using this ICIP number. If the idea is pursued at later date it is considered a new proposal.

**Living** - A special status for ICIPs that are designed to be continually updated and not reach a state of finality. This includes most notably ICIP-1.

## Parts of a ICIP

Each ICIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the ICIP, including the ICIP number, a short descriptive title, a short description, and the author details. The title and description should not a ICIP number.
- Abstract - Abstract is a short paragraph summary.
- Motivation - A motivation section should clearly explain why the current situation inadequate and must be addressed.
- Specification - The technical specification should describe the specifics of the change. The specification should be detailed enough to allow the feature or policy to be implemented without ambiguity.
- Rationale - The rationale motivates the specific proposed solution as opposed to the Motivation which motivates solving the problem.
- Compatibility - This section describes any incompatibilities with previous behavior and how they are handled
- Testint - An optional section containing (some representitive) tests. Tests should either be inlined in the ICIP or included in `../assets/ICIP-###/<filename>`.
- Reference Implementation - An optional section that contains an example implementation.
- Copyright Waiver - Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

## ICIP Formats and Templates

ICIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format. There is a [template](https://github.com/dfinity/ICIPs/blob/main/ICIP-template.md) to follow.

## ICIP Header Preamble

Each ICIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order.

`ICIP`: *ICIP number* (this is determined by the ICIP editor)

`title`: *The ICIP title is a few words*

`description`: *Description is one sentence*

`author`: *The list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

`discussions-to`: *The url pointing to the official discussion thread*

`status`: *Draft, Review, Last Call, Final, Stagnant, Withdrawn, Living*

`last-call-deadline`: *The date last call period ends on* (Optional field, only needed when status is `Last Call`)

`type`: *One of `Informational`, `Standard`, or `Meta`*

`created`: *Date the ICIP was created on*

`requires`: *ICIP number(s)* (Optional field)

`withdrawal-reason`: *A sentence explaining why the ICIP was withdrawn.* (Optional field, only needed when status is `Withdrawn`)

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header lists the names, email addresses or usernames of the authors/owners of the ICIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

It is not possible to use both an email and a GitHub username at the same time. If important to include both, one could include their name twice, once with the GitHub username, and once with the email.

At least one author must use a GitHub username, in order to get notified on change requests and have the capability to approve or reject them.

#### `discussions-to` header

While an ICIP is a draft, a `discussions-to` header will indicate the URL where the ICIP is being discussed.

#### `type` header

The `type` header specifies the type of ICIP: Informational, Standards, or Meta.

#### `created` header

The `created` header records the date that the ICIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `requires` header

ICIPs may have a `requires` header, indicating the ICIP numbers that this ICIP depends on.

## Linking to External Resources

Links to external resources **SHOULD NOT** be included. External resources may disappear, move, or change unexpectedly.

## Linking to other ICIPs

References to other ICIPs should follow the format `ICIP-N` where `N` is the ICIP number you are referring to.  Each ICIP that is referenced in an ICIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references.  The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, the main ICIPs site, mirrors of the main ICIP site, etc.  For example, you would link to this ICIP with `[ICIP-1](./ICIP-1.md)`.

## Auxiliary Files

Images, diagrams and auxiliary files should be included in a subdirectory of the `assets` folder for that ICIP as follows: `assets/ICIP-N` (where **N** is to be replaced with the ICIP number). When linking to an image in the ICIP, use relative links such as `../assets/ICIP-1/image.png`.

## ICIP Editors

The current ICIP editors are those with write access to this repository.

## ICIP Editor Responsibilities

For each new ICIP that comes in, an editor does the following:

- Read the ICIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the ICIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the ICIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the ICIP is ready for the repository, the ICIP editor will:

- Assign an ICIP number (generally the PR number, but the decision is with the editors)
- Merge the corresponding [pull request](https://github.com/dfinity/ICIPs/pulls)
- Send a message back to the ICIP author with the next step.

The ICIP editors monitor ICIP changes, and correct any structure, grammar, spelling, or markup mistakes we see. The editors don't pass judgment on ICIPs. We merely do the administrative & editorial part.

## Style Guide

### ICIP numbers

When referring to an ICIP by number, it should be written in the hyphenated form `ICIP-X` where `X` is the ICIP's assigned number.

### RFC 2119

ICIPs are encouraged to follow [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt) for terminology and to insert the following at the beginning of the Specification section:

> The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

## History

This document was derived heavily from [Etherum's EIP-01](https://github.com/ethereum/EIPs) which was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/). Please direct all comments to the ICIP editors.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
