---
description: >-
  The RFC process is intended to provide a consistent and controlled path for
  changes.
---

# 📬 RFC Process

The "RFC" (request for comments) process is intended to provide a consistent and controlled path for changes (such as new features) so that all stakeholders can be confident about the direction of the project.

Many changes, including bug fixes and documentation improvements can be implemented and reviewed via the normal GitHub pull request workflow.

Some changes though are "substantial", and we ask that these be put through a bit of a design process and produce a consensus among the team.

## When you need to follow this process

You need to follow this process if you intend to make "substantial" changes to the project, or the RFC process itself. What constitutes a "substantial" change is evolving based on team norms and varies depending on what part of the ecosystem you are proposing to change, but may include the following.

* Any semantic or syntactic change that is not a bugfix.
* Removing features, including those that are feature-gated.
* Removing features, including those that are feature-gated.

Some changes do not require an RFC:

* Additions that strictly improve objective, numerical quality criteria (warning removal, speedup, better test coverage, more parallelism, trap more errors, etc.)

If you submit a pull request to implement a new feature without going through the RFC process, it may be closed with a polite request to submit an RFC first.

## What the process is

In short, to get a major change done on the project, one must first get the RFC merged into the RFC space as a page. At that point the RFC is "active" and may be implemented with the goal of eventual inclusion into the project.

* Start a change request in this space
* Copy the [template](broken-reference) page
* Fill in the RFC. Put care into the details: RFCs that do not present convincing motivation, demonstrate lack of understanding of the design's impact, or are disingenuous about the drawbacks or alternatives tend to be poorly-received.
* Submit the change request. As a change request the RFC will receive design feedback from the larger team, and the author should be prepared to revise it in response.
* Build consensus and integrate feedback. RFCs that have broad support are much more likely to make progress than those that don't receive any comments. Feel free to reach out to the RFC assignee in particular to get help identifying stakeholders and obstacles.
* The team will discuss the RFC change request, as much as possible iusing comments in the change request itself. Offline discussion will be summarized on the change request comment thread.
* RFCs rarely go through this process unchanged, especially as alternatives and drawbacks are shown. You can make edits, big and small, to the RFC to clarify or change the design, but make changes as new edits to the change request, and leave a comment on the change request explaining your changes. Specifically, do merge the change request.

## The RFC life-cycle

#### Draft

The first step to getting a change included in the project is to start a draft RFC using a change request.

While in the draft state, the RFC change request will be kept open and can be edited by the author. Review and feedback from the team should not be expected if not asked for.

#### Submitted / In-review

Once the RFC is ready for review, the author should mark the change request as "Ready for review" using the "Submit for review" button.

The team will then [review the RFC and provide feedback](./#reviewing-rfcs). The RFC may be rejected at this stage if the team feels it is not a good fit for the project.

An approved RFC will move to the "Active" state and will be merged into the main branch.

A rejected RFC will move to the "Archive" state.

#### Accepted / Merged / Active

Once an RFC becomes "active" then authors may implement it and submit the feature as a pull request to the project repo. Being "active" is not a rubber stamp, and in particular still does not mean the feature will ultimately be merged; it does mean that in principle all the major stakeholders have agreed to the feature and are amenable to merging it.

Furthermore, the fact that a given RFC has been accepted and is "active" implies nothing about what priority is assigned to its implementation, nor does it imply anything about whether a developer has been assigned the task of implementing the feature. While it is not necessary that the author of the RFC also write the implementation, it is by far the most effective way to see an RFC through to completion: authors should not expect that other project developers will take on responsibility for implementing their accepted feature.

Modifications to "active" RFCs can be done in follow-up change requests. We strive to write each RFC in a manner that it will reflect the final design of the feature; but the nature of the process means that we cannot expect every merged RFC to actually reflect what the end result will be at the time of the next major release.

In general, once accepted, RFCs should not be substantially changed. Only very minor changes should be submitted as amendments. More substantial changes should be new RFCs, with a note added to the original RFC.

#### Archived

RFCs that are not "active" are placed in the "Archive" state. This means the team has decided not to pursue the RFC. The author may re-open a new RFC if another solution has been found worth exploring, this new RFC should reference the archived one.

## Reviewing RFCs

While the RFC change request is up, the team may schedule meetings with the author and/or relevant stakeholders to discuss the issues in greater detail. In either case a summary from the meeting will be posted back to the RFC change request.

The team makes final decisions about RFCs after the benefits and drawbacks are well understood. These decisions can be made at any time, but the team will regularly issue decisions. When a decision is made, the RFC change request will either be merged or closed. In either case, if the reasoning is not clear from the discussion in thread, the team will add a comment describing the rationale for the decision.

## Implementing an RFC

Some accepted RFCs represent vital features that need to be implemented right away. Other accepted RFCs can represent features that can wait until some arbitrary team member feels like doing the work. Every accepted RFC has an associated issue tracking its implementation in the project; thus that associated issue can be assigned a priority via the triage process that the team uses for all issues in the project.

The author of an RFC is not obligated to implement it. Of course, the RFC author (like any other developer) is welcome to post an implementation for review after the RFC has been accepted.

If you are interested in working on the implementation for an "active" RFC, but cannot determine if someone else is already working on it, feel free to ask (e.g. by leaving a comment on the associated issue).
