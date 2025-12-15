# OpenHarmony SIG Governance and Operation Guide
English | [简体中文](./README.md)

This document details the governance and operation guidelines for OpenHarmony Special Interest Groups (SIGs). It aims to provide clear and comprehensive information for community members regarding SIG application, operation, modification, termination, and repository management.

## I. SIG Overview

A SIG is a group of experts and enthusiasts in specific fields within the OpenHarmony community. SIGs aim to promote the development of OpenHarmony in specific technical directions. Each SIG has a clear technical direction and work objectives and uses community collaboration for project development and maintenance.

## II. Applying for a New SIG

### 1. Preparing the Application

Before applying for a new SIG, the applicant needs to:

*   **Read the SIG Governance**： Gain an in-depth understanding of the operating rules of OpenHarmony Community SIGs, including but not limited to:
    *   **SIG Definition and Objectives**: Understand the role and purpose of SIGs in the OpenHarmony community, as well as the problems SIGs aim to solve and the goals they aim to achieve.
    *   **SIG Organizational Structure**: Understand the member roles (e.g., SIG Leader, Committer), responsibilities, and permissions within a SIG.
    *   **SIG Lifecycle**: Be familiar with the entire process of SIG creation, operation, modification, and termination.
    *   **SIG Decision-Making Mechanism**: Understand how decisions are made within a SIG, such as voting mechanisms and consensus mechanisms.
    *   **Relationship between SIG and PMC**: Clarify how the SIG reports to the PMC and how it collaborates with the PMC.
    *   **SIG Communication and Collaboration Methods**: Understand how SIG members communicate and collaborate effectively, such as mailing lists, regular meetings, and code reviews.
    *   **SIG Code of Conduct**: Abide by the OpenHarmony community's code of conduct and maintain a good community atmosphere.
    *   You can learn about the operating rules of SIGs by carefully reading other sections of this document.
*   **Confirm the Uniqueness and Feasibility of the Technical Direction**:
    *   Ensure that the proposed technical direction does not already exist within the OpenHarmony community.
    *   Review the [existing SIG list](https://gitcode.com/openharmony/community/tree/master/sig) and the [historical DEV mailing list](https://lists.openatom.io/hyperkitty/list/dev@openharmony.io/).
    *   Confirm that the proposed technical project can eventually be transformed into new components and sub-projects of OpenHarmony.
    *   If you have any questions, you can consult the PMC through the mailing list [dev@openharmony.io](mailto:dev@openharmony.io).
*   **Prepare SIG Related Documents**: Refer to the [SIG Application Template](../meeting-notes/docs/openharmony_sig_template.pptx) and prepare the SIG charter and other documents.
*   **Define the SIG's Goals and Scope**: Clearly define the SIG's objectives, scope, and expected outcomes.

### 2. Submitting the Application

*   **Create a Draft SIG Proposal**: Write a proposal according to the [SIG Application Template](../meeting-notes/docs/openharmony_sig_template.pptx).
*   **Submit the SIG Application Issue**: Submit the [application issue](https://shimo.im/sheets/16q8xyRaR9creOq7/MODOC) to the OpenHarmony PMC to initiate the SIG establishment application.

### 3. PMC Proposal Review

*   The SIG initiator introduces the proposed SIG at the PMC regular meeting, explaining the SIG's goals, significance, and plans.
*   The PMC reviews the establishment of the SIG, including assessing the technical direction, feasibility, relationship with existing SIGs, and other aspects, and decides whether to approve the establishment of the SIG and related SIG repositories and communication channels.
*   The review meeting forms meeting minutes, recording the PMC's review opinions.  These minutes must be attached when creating the SIG group.

### 4. Creating the SIG Group

After the PMC approves the application, the SIG initiator performs the following operations:

*   **Fork the Code Repository**: Fork the OpenHarmony community code repository to your personal repository.
*   **Create the SIG Directory**: Create your own SIG directory under the `sig` directory.
*   **Copy the SIG Template**: Copy the SIG application template (`sig_template`) to this directory.
*   **Fill in the SIG Information**: Fill in the SIG information according to the actual situation. You can refer to the descriptions of existing SIGs.
    ```
    git clone https://gitee.com/YOURGITEE/community
    cd ./community/sig
    cp -r sig_template sig_YOURSIGNAME
    cd sig_YOURSIGNAME
    mv sig_template_cn.md sig_YOURSIGNAME_cn.md
    mv sig_template.md sig_YOURSIGNAME.md
    vim sig_YOURSIGNAME_cn.md
    vim sig_YOURSIGNAME.md
    ```
*   **Configure SIG Organizational Information**: Edit the `sig/sigs_list.toml` file to configure the SIG organizational information.

## III. SIG Operation

### 1. SIG Repositories and Communication Channels

*   SIGs use the OpenHarmony community's unified infrastructure (Gitee repositories and mailing lists) for work and communication.
*   For the process of creating, renaming, and retiring repositories, please refer to the "**Repository Management**" section of this document.
*   SIG Mailing List Creation: Contact **[xzmu@openatom.org](mailto:xzmu@openatom.org)** and attach the meeting minutes approving the SIG. Provide the mailing list name and administrator email address (usually the SIG leader).
*   The SIG leader should ensure the effective operation of the SIG repositories and communication channels and respond to community feedback in a timely manner.

### 2. SIG Meetings

*   SIGs should hold regular public meetings (online or offline) to maintain information synchronization and collaboration among SIG members.
*   The convener should notify members of the meeting time, location, and agenda in advance to ensure the effectiveness of the meeting.
*   The meeting agenda should include progress reports, discussion of issues, and decision-making, covering all aspects of the SIG's work.
*   Meeting minutes should record key points, discussion results, and decisions, and be shared and published to the corresponding mailing list in a timely manner (if there is no independent mailing list, the DEV mailing list can be reused) to maintain transparency.

### 3. SIG Management

*   The SIG leader is responsible for the normal operation and management of the SIG and maintains communication and collaboration with the PMC.
*   The leader determines the SIG's work direction, task allocation, and member joining, ensuring the achievement of the SIG's goals.
*   The leader regularly reports the SIG's work progress and results to the PMC and community members, keeping information open and transparent.
*   The leader can organize working groups or task forces as needed to coordinate member work and promote project progress.
*   If necessary, the leader can submit an application to the PMC to modify or terminate the SIG, providing sufficient reasons.
*  The SIG group needs to hold regular meetings to discuss and summarize the work in SIG's area, and report to the OpenHarmony PMC regularly. If the leader role in the SIG changes, it is necessary to inform the OpenHarmony PMC members in time, and adjust the organization information and repository permissions accordingly.

## IV. SIG Modification and Termination

*   **SIG Modification**: Includes changes in leadership, adjustments in work direction, and redistribution of tasks. Modifications require notification to the PMC and SIG members and are determined after full consultation and discussion.
*   **SIG Termination**: The leader submits a termination application to the PMC and provides sufficient reasons and explanations. The PMC will evaluate the termination application and make the final decision on the termination of the SIG.

## V. Repository Management

### 1. OpenHarmony Project Repository Management Process

The OpenHarmony project goes through the following steps from open source repository creation to incubation and graduation into the mainline:

1.  **Declare an Architecture SIG New Repository Application Issue**: Submit an application for a new repository.
2.  **Declare an Architecture SIG Incubation Graduation Pre-review Issue**: Conduct a pre-review for incubation graduation.
3.  **Declare a QA SIG Incubation Graduation Final Review Issue**: Complete the final review for incubation graduation and resolve all outstanding issues.

**Precautions**:

*   **Incubation Graduation Conditions**: Meet basic compliance requirements and complete the joint construction of the associated repositories for the incubation repository.
*   **Cross-Code Review**: The new repository must be configured with at least 2 or more Committers to support the cross-code review function.

### 2. SIG Group Repository Addition, Retirement, and Renaming Application

1.  **Apply for Architecture SIG Review**:
    *   Addition, Retirement, Renaming: Refer to [Template 1 - Addition, Retirement, Renaming](../sig/sig_architecture/meetings/repository_review_template.pptx).
    *   Open Source Software Introduction: Refer to [Template 2 - Open Source Software Introduction](../sig/sig_architecture/meetings/OpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx).
    *   Apply for [Architecture SIG](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC) issue review.
2.  **New Repository Electronic Flow Application**: After the Architecture SIG review is passed, refer to the [Operation Guide](http://dcp.openharmony.cn/workbench/ciCommunity): "Operation Guide" --> "SIG Management" --> "SIG Repository Application".
3.  **Repository Retirement and Renaming Electronic Flow Application**: After the Architecture SIG review is passed, refer to the [Operation Guide](http://dcp.openharmony.cn/workbench/ciCommunity): "Operation Guide" --> "SIG Management" --> "Repository Management".

### 3. Repository Incubation Graduation

1.  **Apply for Architecture SIG Incubation Pre-review**: [Apply for an issue](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC) and refer to the [template](../sig/sig_architecture/meetings/repository_review_template.pptx).
2.  **Apply for Quality SIG Incubation Graduation Review**: [Apply for an issue](https://shimo.im/sheets/AQrrKb4pJCUFYkHR/MODOC) and refer to the [graduation standards](../sig/sig_qa/guidance_for_incubation_project_graduation_cn.md).
3.  **Submit the Repository Incubation Graduation Electronic Flow**: After the Quality SIG graduation review is passed, submit the [incubation graduation electronic flow](http://dcp.openharmony.cn/workbench/ciCommunity): "Operation Guide" --> "SIG Management" --> "Incubation Report".