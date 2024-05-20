# Overview & Rationale

Climate Informatics, like many other communities and fields, has software at its heart. Underlying most publications is a novel piece of software playing some critical role, e.g., embodying a model, processing or analysing data, or producing a visualisation. In order for such software artefacts to have the most impact, they should be available, functional, and reusable, such that other researchers can benefit from the work, verify the claims of the paper, and then build upon the software to do more great work. These ideals are summarised by the FAIR principles of data, which can be applied to software: research software should be Findable, Accessible, Interoperable, and Reusable. In order to help promote [FAIR software](https://www.nature.com/articles/s41597-022-01710-x), Climate Informatics is embarking, for the first time, on an _Artefact Evaluation phase_ for full paper submissions, after those submissions have been accented for publication as the conference proceedings in [Environmental Data Science](https://www.cambridge.org/core/journals/environmental-data-science) following the traditional peer-review process. Artefact Evaluation provides an opportunity to embed the values of reproducibility into the publication process in a lightweight opt-in fashion, thus encouraging authors to make software available and the results of the paper reproducible.

A committee of reviewers, the Artefact Evaluation Committee (AEC), will review the submitted artefacts against three [criteria](./badges): is the software available? is it functional, and can it be used to reproduce the (central) claims or thesis of the paper?

# Timeline and Process

Authors of full-papers that are accepted to the Cambridge University Press (CUP) journal proceedings will be encouraged (but not required) to submit supporting materials for Artefact Evaluation following the Climate Informatics conference, with a deadline of: 12th September.

The Artefact Evaluation Committee will review the artefacts, assessing whether they are functional (can be run) and whether the central results of the paper can be reproduced. The reviewers will interact with the authors to suggest how to improve the reproducibility if any issues are discovered.

Reviewing will take place over 5 weeks.

# [Badges and Evaluation Criteria](https://github.com/alan-turing-institute/climate-informatics-2024-ae/blob/main/badges.md)

# Publishing workflow

We want to avoid deincentivising authors who opt into the reproducibility challenge by having this lead to a slower timeline to publication. For those papers that opt-in, we will therefore publish them initially without the badges (so as not to delay the timeline to publication) and at a later date, after artefact evaluation, publish an addendum and retrospectively update the article with the badge(s).

(In the CUP platform is there is no functionality for versioning articles. However, there is a precedent for retrospectively updating a published article with a badge by using an addendum. See for example https://doi.org/10.1017/dap.2022.5. In this case it was a mistake: the original article (https://doi.org/10.1017/dap.2021.38) wasn’t awarded Open Data and Open Materials badges when it should have been. So we published the addendum and retrospectively updated the original article and Data Availability Statement with the badges.)

# Guidelines for Reviewers

Reviewers will be recruited to the AEC from the [Climate Informatics community](http://www.climateinformatics.org) (join [here](https://groups.google.com/g/climate-informatics-news)) and [Turing Environment and Sustainability Grand Challenge community](https://cassgvp.kumu.io/alan-turing-institute-environment-and-sustainability) (join [here](https://forms.office.com/pages/responsepage.aspx?id=p_SVQ1XklU-Knx-672OE-ZmEJNLHTHVFkqQ97AaCfn9UMTZKT1IwTVhJRE82UjUzMVE2MThSOU5RMC4u)). Please join either (or both!) communities to receive updates on reviewer training opportunities.

## Requirements for reviewers
We require a minimum level of practical experience in climate data science to participate as a reviewer. This ensures that the review process can focus on technical detail rather than computational literacy. Reviewers will be required to evidence their experience through their own software publications. Full reviewer requirements will be published ==XXX==

## Expected workload

- Each reviewer will be assigned 2 submissions
- 2-hour on-boarding session to get everyone up to speed
- Each review can be expected to take 8 hours to complete, including direct communications with the submitting author via our review portal
- Final reviews should be submitted by TBD (mid October)

## Benefits to reviewers
Reviewers will benefit from hands-on training in high fidelity computational reproducibility, which we anticipate will support their own development of reproducible research artefacts. Reviewers will be able to reference their contribution as evidence of leadership culture change towards reproducibility, and invited to co-author a [retrospective report](#retrospective-report) to be published in [Environmental Data Science](https://www.cambridge.org/core/journals/environmental-data-science) after the review process is complete. They will be [supported](#support) by the CI Reproducibility team and AEC throughout, thereby strengthening their connections with this highly skilled team.

##  Evaluation process

Reviewers will asses the artefacts against a checklists provided for each ["badge" level to be awarded](https://github.com/alan-turing-institute/climate-informatics-2024-ae/blob/main/badges.md).

For each point, reviewers will be required to briefly note the evidence for this point, anything they have done to validate that point (e.g., what did you need to reproduce a claim), as well as the outcome (negative, neutral, or positive) and a brief reason for their judgment.

## Feedback to the authors

This process has been designed to be collaborative and iterative. During the first 3 weeks, reviewers will be able to feed-back to authors.
Authors will be encouraged to push improvements to the artefact whenever possible. For example, if essential documentation is missing, then rather than submitting a negative evaluation or providing only the reviewers with the required information, the authors should provide that information via a versioned updated to the artefact.

# Author submission guidelines

## What authors should provide in their artefact submission

Artifact submissions require three parts, as described below. ==Authors will be invited to attend reviewer training, to receive full guidance on the expectations and processes for submission described below.==

1. An overview of the artifact.

2. A non-institutional URL (or more, e.g. one for the code and one for the data) pointing to either: a single file containing the artifact (recommended), or the address of a public source control repository. The URL must be non-institutional to protect the anonymity of reviewers. Acceptable URLs can be obtained from Google Drive, Dropbox, Gitlab, Zenodo, and other providers. URLs may be generated using reviewer-only links. ==Do we prefer a versioned URL (e.g. DOI) here, or is that only expected if "accessible"==

3. A hash certifying the version of the artifact at submission time: either an md5 hash of the single file (use the md5 or md5sum command-line tool to generate the hash), or the full commit hash for the repository (e.g., from git reflog --no-abbrev).

Artifacts do not need to be anonymous as reviewers will be aware of author identities.

The overview should be a document (markdown, text, or PDF) consisting of the following parts:

1. Introduction briefly explaining the purpose of the artifact and how it supports the paper.

2. Hardware requirements to evaluate the artifact. If the artifact requires specific hardware (e.g., many cores, disk space, GPUs, specific processors), please provide instructions on how to gain access to the hardware (it may be required that a video call is scheduled if, e.g., access to a cluster cannot be granted but some aspects can be presented over a call).

3. A Getting Started guide, giving instructions for setup and basic testing. List any software requirements. The instructions should take roughly 30 minutes to complete. Reviewers will follow the guide during an initial kick-the-tires phase and report issues as they arise. The Getting Started Guide should be as simple as possible, and yet it should stress the key elements of your artifact. Anyone who has followed the Getting Started Guide should have no technical difficulties with the rest of your artifact.

4. Step-by-Step Instructions for how you propose to evaluate the functionality of your artifact (with appropriate connections to the relevant sections of your paper) and reproduce any experiments or other activities that support the conclusions in your paper. You should:

* List all claims in the paper and state whether or not each is supported.

    - For supported claims, say how the artifact provides support and how to produce these results. Explain the expected outputs and how to interpret the outputs relative to the paper. If there are any expected warnings or error messages, explain those as well. Ideally, artifacts should include sample outputs and logs for comparison.

    - For unsupported claims, explain why they are omitted. For example, this can be reasonable if it requires very long runs on clusters, or involves data sets that are proprietary. In this case, the authors should provide some mechanism by which claims can be tested by some other mechanism to establish the veracity of the approach, e.g., a smaller run or a different sample data set, with expected outputs.

* Please indicate how long you expect any runs to take that will typically take more than half a minute.

It can be useful to describe how to perform runs on smaller input data sets. Reviewers may choose to run on smaller inputs or larger inputs depending on available resources.

5. A Reusability Guide for how you propose to evaluate the reusability of your artifact. Explain which parts of your artifact constitute the core pieces which should be evaluated for reusability. Explain how to adapt the artifact to new inputs or new use cases. Provide instructions for how to find/generate/read documentation about the core artifact. Articulate any limitations to the artifact’s reusability.

When packaging your artifact, please keep in mind: a) how accessible you are making your artifact to other researchers, and b) the fact that the artefact committee members have a limited time.

A good way to package artifacts is as a virtual machine (VM). VMs give an easily reproducible environment that is somewhat resistant to bit rot. They also give reviewers confidence that errors or other problems cannot cause harm to their machines. Source code artifacts should use Docker or another build tool to manage all compilation and dependencies. This improves the odds that the reviewers will be able to quickly and painlessly install the artifact — without getting lost in environment issues ([e.g. what Python do I need?!](https://xkcd.com/1987/)).

# Support

There will be a 1-hour informal session for authors ==and reviewers== who are considering submitting artefacts to give an overview of the approach. This will happen online after CI 2024.

There will also be a panel about reproducibility at CI2024 which will provide some motivation and inspiration.

The artefact chairs are available to ask any questions about the process or to ask advice about preparing the artefact or if any parts of the process are unclear.

# Retrospective report

The reproducibility chairs will produce a general report after the artefact evaluation process documenting the approach and reporting on experiences. Reviewers ==and authors== will be invited to co-author the report, providing their experiences. Any experiences will be anonymised however with respect to the artefacts.
