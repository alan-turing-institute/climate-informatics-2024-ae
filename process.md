# Overview & Rationale

Climate informatics, like many other communities and fields, has software at its heart. Underlying most publications is a novel piece of software playing some critical role, e.g., embodying a model, processing or analysing data, or producing a visualisation. In order for such software artefacts to have the most impact, they should be available, functional, and reusable, such that other researchers can benefit from the work, verify the claims of the paper, and then build upon the software to do more great work. These ideals are summarised by the FAIR principles of data, which can be applied to software: research software should be Findable, Accessible, Interoperable, and Reusable. In order to help promote [FAIR software](https://www.nature.com/articles/s41597-022-01710-x), Climate Informatics is embarking, for the first time, on an _Artefact Evaluation phase_ following the standard peer-review process. Artefact Evaluation provides an opportunity to embed the values of reproducibility into the publication process in a lightweight opt-in fashion, thus encouraging authors to make software available and the results of the paper reproducible.

A committee of reviewers, the Artefact Evaluation Committee (AEC), will review the submitted artefacts against three criteria: is the software available? is it functional, and can it be used to reproduce the (central) claims or thesis of the paper?

# Timeline and Process

Authors of full-papers that are accepted to the Cambridge University Press (CUP) journal proceedings will be encouraged (but not required) to submit supporting materials for Artefact Evaluation following the Climate Informatics conference, with a deadline of: XXXX.

The Artefact Evaluation Committee will review the artefacts, assessing whether they are functional (can be run) and whether the central results of the paper can be reproduced. The reviewers will interact with the authors to suggest how to improve the reproducibility if any issues are discovered.


Reviewing will take place over 6 weeks.

# [Badges and Evaluation Criteria](https://github.com/alan-turing-institute/climate-informatics-2024-ae/blob/main/badges.md)

# Publishing workflow

We want to avoid deincentivising authors who opt into the reproducibility challenge by having this lead to a slower timeline to publication. For those papers that opt-in, we will therefore publish them initially without the badges (so as not to delay the timeline to publication) and at a later date, after artefact evaluation, publish an addendum and retrospectively update the article with the badge(s).

(In the CUP platform is there is no functionality for versioning articles. However, there is a precedent for retrospectively updating a published article with a badge by using an addendum. See for example https://doi.org/10.1017/dap.2022.5. In this case it was a mistake: the original article (https://doi.org/10.1017/dap.2021.38) wasn’t awarded Open Data and Open Materials badges when it should have been. So we published the addendum and retrospectively updated the original article and Data Availability Statement with the badges.)

# Guidelines for Reviewers

## Expected workload

- 16 submissions, 2 reviewers per AE submission, 2 submissions per reviewer (so AEC of up to 16 reviewers)
- 2-hour on-boarding session to get everyone up to speed

##  Evaluation process

Follow the checklists provided for each ["badge"](https://github.com/alan-turing-institute/climate-informatics-2024-ae/blob/main/badges.md).

For each point, please briefly note what is the evidence for this claim, briefly noting anything you have done to validate that point (e.g., what did you need to reproduce a claim), as well as the outcome (negative, neutral, or positive) and a brief reason for your judgment.

## Feedback to the authors

Authors should be encouraged to push improvements to the artefact whenever possible. For example, if essential documentation is missing, then rather than just providing the reviewers with the required information, the authors should provide that information via an updated artefact.

# Submitter guidelines

## What authors should provide in their artefact submission

Artifact submissions require three parts:

1. An overview of the artifact.

2. A non-institutional URL pointing to either: a single file containing the artifact (recommended), or the address of a public source control repository. The URL must be non-institutional to protect the anonymity of reviewers. Acceptable URLs can be obtained from Google Drive, Dropbox, Gitlab, Zenodo, and other providers.

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

There will be a 1-hour informal session for authors who are considering submitting artefacts to give an overview of the approach. This will happen online after CI 2024.

There will also be a panel about reproducibility at CI2024 which will provide some motivation and inspiration.

The arteface chairs are available to ask any quetions about the process or to ask advice about preparing the artefact or if any parts of the process are unclear.

# Retrospective report

The reproducibility chairs will produce a general report after the artefact evaluation process documenting the approach and reporting on experiences. Reviewers will be invited to co-author the report, providing their experiences. Any experiences will be anonymised however with respect to the artefacts.
