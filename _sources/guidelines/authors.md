(guidelines-authors)=

# Guidelines for Authors

## What authors should provide in their artifact submission

Artifact submissions require three parts, as described below. 

1. An overview of the artifact.

2. A non-institutional URL (or more, e.g. one for the code and one for the data) pointing to either: a single file containing the artifact (recommended), or the address of a public source control repository. The URL must be non-institutional to protect the anonymity of reviewers. Acceptable URLs can be obtained from Google Drive, Dropbox, Gitlab, Zenodo, and other providers. URLs may be generated using reviewer-only links.

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

5. A Reusability Guide for how you propose to evaluate the reusability of your artifact. Explain which parts of your artifact constitute the core pieces which should be evaluated for reusability. Explain how to adapt the artifact to new inputs or new use cases. Provide instructions for how to find/generate/read the documentation about the core artifact. Articulate any limitations to the artifact’s reusability.

When packaging your artifact, please keep in mind: a) how accessible you are making your artifact to other researchers, and b) the fact that the artifact committee members have a limited time.

A good way to package artifacts is as a virtual machine (VM). VMs give an easily reproducible environment that is somewhat resistant to bit rot. They also give reviewers confidence that errors or other problems cannot cause harm to their machines. Source code artifacts should use Docker or another build tool to manage all compilation and dependencies. This improves the odds that the reviewers will be able to quickly and painlessly install the artifact — without getting lost in environment issues ([e.g. what Python do I need?!](https://xkcd.com/1987/)).

## Support

There was a 1-hour informal session on 20th May, 2024 for authors who are considering submitting artifacts to give an overview of the approach. The recording is available [here](https://drive.google.com/file/d/1A21CuzRpe7sQcTgc5Hza3Vp5EAWVcmH3/view?usp=sharing).

We also organised a panel about reproducibility at CI2024 which provided some motivation and inspiration. The recording is available [here](https://youtu.be/_cJGsfoKo0w?feature=shared).

The artifact chairs are available to ask any questions about the process or to ask advice about preparing the artifact or if any parts of the process are unclear.