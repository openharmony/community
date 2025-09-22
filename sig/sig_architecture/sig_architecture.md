# sig_architechture

[简体中文](./sig_architecture_cn.md) | English

**Note**: The content of this SIG follows the conventions described in the OpenHarmony PMC Management Charter [README](/zh/pmc.md).

## SIG Goals and Scope

### Goals

To establish OpenHarmony's architectural design principles, oversee the definition, design, evolution, and governance of the OpenHarmony architecture, and to create clear processes and standards for architectural reviews and SIG incubation/graduation.

### Scope

- Responsible for the evolution of the overall OpenHarmony architecture, and for reviewing and making decisions on architectural changes, including the addition, merging, splitting, and removal of subsystems, components, and repositories.
- Responsible for revising and maintaining core architectural documents such as the *Architectural Design Principles* and the *OpenHarmony System Architecture*.
- Defining and overseeing the architectural acceptance criteria for SIGs (or new features, subsystems) from incubation to graduation, and organizing the corresponding reviews.
- Providing the [Third-Party Open-Source Software Selection and Evaluation Template](https://www.google.com/url?sa=E&q=meetings%2FOpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx).

## SIG Incubation and Graduation Criteria

To ensure the healthy and sustainable development of all technical directions within OpenHarmony, the Architecture SIG is responsible for the architectural governance and acceptance of newly incubated SIGs (or features, subsystems, etc.). The following are the fundamental architectural acceptance criteria that a SIG must meet to graduate from incubation:

| Acceptance Criterion | Specific Requirements |
| :--- | :--- |
| Supported Business | <ul><li> The business case is based on clear user requirements or community consensus. It must be general-purpose and serve a wide range of scenarios, rather than being custom-built for a specific customer or use case. |
| Architectural Soundness | <ul><li>Clear Layering: The architectural design aligns with the community's overall layering logic, and its position within the system's layers is appropriate.</li><li>Well-Defined Dependencies: Dependencies between modules are clear, reasonable, free of circular dependencies, and avoid inappropriate cross-layer calls.</li><li>High Cohesion, Low Coupling: Functional units (modules/components) are reasonably divided, with highly related internal functions and low coupling between modules, facilitating independent evolution and maintenance.</li></ul> |
| Quality Attributes Met | <ul><li>Clear Definitions: Key quality attributes such as memory footprint, ROM usage, performance, reliability, testability, maintainability, and extensibility have clear and reasonable quantitative metrics.</li><li>Achieved Targets: There is test data or practical evidence demonstrating that all quality attribute metrics have met their predefined targets.</li></ul> |
| Functional Completeness | <ul><li>Core Feature Coverage: Core functionalities are fully implemented to meet the basic needs of the target scenarios.</li><li>Broad Scenario Adaptability: It can be adapted to mainstream application scenarios in its target domain.</li><li>Extensibility: Provides necessary extension mechanisms (e.g., plugins, configurations, APIs). The secondary development effort required for users to solve the vast majority of problems in the target domain is comparable to that of mainstream solutions in the industry.</li></ul> |
| Technical Maturity | <ul><li>Key technical solutions are supported by mature practices, integration and commercial use by multiple external users or downstream vendors.</li><li>Availability of clear user feedback, usage reports, or commercial case studies, which may include details on effectiveness, performance data, and suggestions for improvement.</li></ul> |
| Documentation Completeness | <ul><li>Repository Documentation: The `README.md` file in each repository should include a functional introduction, a logical architecture diagram, build instructions, and its interaction with other repositories.</li><li>User Documentation: Comprehensive developer guides, API reference manuals (if applicable), and sample code (Samples/Codelabs) for typical scenarios are provided.</li><li>Quality Standards: The documentation structure is clear, the content is accurate and comprehensive, and the examples are runnable, effectively guiding developers to get started quickly.</li></ul> |
| System Compatibility | <ul><li> For developer-facing features (e.g., APIs, binary interfaces, file formats), their compatibility requirements must be clearly stated in the compatibility specification documents and defined in the system capabilities (syscaps) to ensure compatibility during system upgrades and application development. |
| API Design Soundness | <ul><li> For repositories that provide APIs, the API design must adhere to the community's unified specifications and receive formal evaluation and approval from the API SIG. |

## SIG Members

### Leaders

- @im-off-this-week([https://gitee.com/im-off-this-week](https://gitcode.com/im-off-this-week))

### Meetings

- **Time**: Every Tuesday at 9:30 AM
- **Meeting Proposal**: [OpenHarmony SIG-Architecture Meeting Proposal](https://shimo.im/sheets/StzhuFkEk38enrnl/MODO)
- **Meeting Link**: Welink
- **Meeting Invitation**: Please [subscribe](https://lists.openatom.io/postorius/lists/dev.openharmony.io) to the dev@openharmony.io mailing list to receive meeting invitations.
- **Meeting Minutes**: [View historical meeting minutes](https://gitee.com/openharmony/community/tree/master/sig/sig_architecture/meetings)

### Contact

- **Mailing List**: [dev@openharmony.io](https://www.google.com/url?sa=E&q=mailto%3Adev@openharmony.io)
- **WeChat Group**: NA