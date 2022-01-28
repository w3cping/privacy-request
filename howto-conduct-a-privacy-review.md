# How to Conduct a PING Privacy Review
(or, "what to expect when you're inspecting a spec")


## Questions and Concerns
This document is managed by the <abbr name="Privacy Interest Group">PING</abbr>
chairs and <abbr name="World Wide Web Consortium">W3C</abbr> staff. Please feel
free to reach out with any questions or concerns you have. The current leads
of PING are (in alphabetical order):

- Nick Doty (ndoty@cdt.org, <abbr name="Center for Democracy and Technology">CDT</abbr>)
- Christine Runnegar (runnegar@isoc.org, <abbr name="Internet Society">ISOC</abbr>)
- Wendy Seltzer (wseltzer@w3.org, W3C Strategy Lead)
- Peter Snyder (pes@brave.com, Brave Software)
- Samuel Weiler (weiler@w3.org, W3C Security and Privacy Strategist)


## Goals
This document is intended to provide a guide for how the PING review process
works, and procedurally how to find, conduct and complete a PING privacy review.
This document does not describe the *substance* of a review, or the kinds of
issues to look for in a spec you're reviewing (though if you have questions
about about the substance of a review you're conducting, please feel
free to reach out to the PING chairs anytime).


## Stages of a PING Review
The following subsections describe the different steps in conducting a review,
including how to [find a specs to review](#finding-new-proposals),
[where to find the proposed spec text to review](#reviewing-a-spec),
[how to share your findings on a PING call](#presenting-a-review),
and [how to present your findings with the proposed spec's authors](#finishing-a-review).


### <a id="finding-new-proposals" />1. Identifying Proposals To Review
The privacy review process begins by a group formally requesting a privacy
review from PING. Groups request a review by creating an issue
in PING's [privacy-request repo on GitHub](https://github.com/w3cping/privacy-request/).
New requests will appear as [open issues](https://github.com/w3cping/privacy-request/issues).

When PING receives a new request, the PING chairs will usually send a message
out to all PING members to see if anyone volunteers to perform the review,
though sometimes PING chairs may conduct the review themselves, or approach
area experts directly. If you see a new review request for a proposal
you'd like to review though, feel free to contact a PING chair and let them
know. Most likely this will make their day and they'll happily assign the
review to you.

Usually a proposal is reviewed by just one PING member, though occasionally
two or more PING members may collaborate on a review. This is more common
when a proposed spec is very long, highly technical, or one of the reviewers
are new to the process.

PING keeps track of which reviewer(s) are reviewing which spec by using the
"assigned to" field on each privacy-request issue.
[Review #56](https://github.com/w3cping/privacy-request/issues/56), for example,
was reviewed by three reviewers.

PING communication is mostly done over Slack. If you would like to participate
in reviews, but are not on the PING slack, please contact a PING chair.


### <a id="reviewing-a-spec" />2. Conducting the Review
Once you've been assigned a privacy review, you can find the of the proposed
spec to review in the text of the privacy-review issue. For example,
[privacy-request #56](https://github.com/w3cping/privacy-request/issues/56)
is a request from the [W3C Web Payments Working Group](https://www.w3.org/Payments/WG/),
requesting a review of the [Secure Payment Confirmation](https://w3c.github.io/secure-payment-confirmation/)
proposal, the URL of which is https://w3c.github.io/secure-payment-confirmation/.

Your review should focus on the text of the proposed spec. However, you might
find additional, complementary resources helpful to understand the goals
and methods used in the proposal. Often the working group requesting the review
will include links to additional resources in the privacy-request issue.
For example, in [privacy-request #56](https://github.com/w3cping/privacy-request/issues/56),
the working group included a link to an "explainer" (or a high level, less
technical document summarizing the aims and means of the more technical document).
The URL of that explainer is https://github.com/w3c/secure-payment-confirmation/blob/main/explainer.md.

When reviewing the proposal, you should take care to read the entire proposal.
A comprehensive list of technical issues to consider is beyond the scope
of this document, but the W3C's [Security and Privacy Self-Review Questionnaire](https://w3ctag.github.io/security-questionnaire/)
(co-maintained by the W3C <abbr name="Technical Architecture Group">TAG</abbr> and PING)
may be helpful in identifying questions and issues to consider during your review.

Note the issues you identify during your review for later discussion. Issues
could either be specific issues you've identified, or general concerns
you're not sure about and would like to discuss with other members in PING.


### <a id="presenting-a-review" />3. Presenting Your Review to PING
The next step is to present your findings to the rest of PING, usually by
joining one of PING's bi-weekly calls. Information for when PINGs calls are, and
how to join those calls, are on the [PING home page](https://www.w3.org/Privacy/IG/).
A PING chair will work with you to add your review to a meeting agenda.

Presenting a review on a call is an informal process, and most of the
time members of the working group proposing the spec *are not* on the call.

The review discussion process starts with the reviewer(s) summarizing 
the proposed spec to the rest of PING. These summaries are generally high
level, and not intended to on the level of describing specific method calls
or implementation algorithms. The goal is to provide the rest of PING with
an understanding of the goals of the proposal, and enough background to
understand the privacy issues you've identified (and to suggest additional
possible areas of concern).

Next, reviewers describe each privacy issue they identified during their
review. These might be issues the reviewer is confident about, or concerns
the reviewer was unsure about, and wanted to bring to PING's attention for
further discussion and consideration. PING as a group will discuss each issue
as needed.

After discussion, the reviewer will retain, discard, or alter the privacy
issues they've identified as the reviewer sees fit. **Note that issues
from privacy reviews are filed as individuals, not collectively by PING
as a group.** This means that PING members may disagree on the results
of a privacy review, or might even file contradictory privacy issues if
PING members disagree. In the case that a PING privacy review results in 
contradictory (or mutually exclusive) issues being filed, its the responsibility
of the working group making the proposal (and, ultimately the director)
to figure out how to proceed.


### <a id="finishing-a-review" />4. Documenting Your Review
The final step in the review process is to present your findings to the
working group that requested the review in the first place. This
is done in several steps.

**First**, create GitHub issues for each privacy issue you identified in the
proposal's repo *not on the PING privacy-request issue*; the PING
privacy-request repo keeps track of privacy review requests PING receives, but
the substance of those reviews (i.e., the issues that need to be addressed
in the proposed spec) must be filed in the repo for the proposed spec.
For example, [privacy request #56]([Review #56](https://github.com/w3cping/privacy-request/issues/56)
is an issue in PING's privacy-request repo, but issues resulting for the review
should be filed in the [Secure Payment Confirmation repo](https://github.com/w3c/secure-payment-confirmation/issues).

Create one issue in the working group's repo for each privacy issue you
identified. We suggest starting each filed issue by noting i) that the issue
was the result of a PING privacy review, and ii) with a link back to
the privacy-requests issue requesting the privacy review. See, for example,
the first line of [this issue](https://github.com/w3c/imsc-hrm/issues/28).

Each privacy issue you create should include the following:

- A brief and succinct description of the privacy issue you identified
- If applicable, what resolution you think would be appropriate to solve / address
  the issue. It **is not** your responsibility to suggest a solution to the
  problem you identified (i.e., you don't need to provide a solution to the privacy
  vulnerability), though it can be helpful to say what criteria you would judge
  a solution by. For example, if you identify new browser fingerprinting
  surface exposed by proposed spec, its helpful to say "this issue would be
  resolved by preventing fingerprinting scripts from accessing this information",
  but its not your responsibility to say "the spec should prevent fingerprinting
  scripts from accessing this information through methods X, Y, and Z."
- Add either a `privacy-tracker` or `privacy-needs-resolution` label to the
  issue (but not both). The `privacy-tracker` label denotes that you want
  to bring the issue to the group's attention, but don't think the issue is
  critical. The `privacy-needs-resolution` label denotes that you think the
  identified issue is critical, and that the proposal should not continue
  through the standardization process until the issue is addressed.

Second, once you've created an issue in the proposed spec's repo for each
privacy concern you've identified, add a comment on the original
privacy-requests issue summarizing your review. This summary can be just
a list of issues you've identified; it does not need to include additional
text. [This comment on the review of the IMSC-HRM proposal](https://github.com/w3cping/privacy-request/issues/65#issuecomment-1006978947)
gives an example of such a review-summary comment.

Third and finally, mark the privacy review complete by closing the
privacy-requests issue.


### <a id="following-up" />5. Following Up on a Review
At this point you've successfully completed a PING privacy review.
Congratulations! The working group will respond to the issues you filed,
and hopefully thank you for your review. You are encouraged (though not
required) to continue discussing the privacy issues you filed with the working
group, as they try to understand, and then correct, the privacy issues you
identified.

Sometimes working groups will not agree with your issues, and thats okay.
However though, working groups should never close an issue you filed
until you agree that the issue has been satisfactorily resolved. If a working
group does close an issue in a way or for a reason you don't agree with,
please notify or involve a PING chair or team leader, who will gladly
get involved to try and address the situation.

Finally, if for whatever reason you are not able or interested in continuing
the discussion around an issue you field, please also notify a PING chair
or team leader. We understand that obligations and availability change over time,
and we'll be glad to work with you to transfer ownership of an issue to someone
else.


## Links And Resources
- [PING Home Page](https://www.w3.org/Privacy/IG/)
- [PING "Privacy Requests" Repo](https://github.com/w3cping/privacy-request/)
- [Self-Review Questionnaire: Security and Privacy](https://w3ctag.github.io/security-questionnaire/)
- [Privacy Anti-Patterns in Standards](https://www.w3.org/blog/2019/06/privacy-anti-patterns-in-standards/)
- [PING Signup Form](https://www.w3.org/2004/01/pp-impl/52497/join)
- [Open Privacy Tracking Issues](https://w3c.github.io/horizontal-issue-tracker/?repo=w3cping/tracking-issues)
