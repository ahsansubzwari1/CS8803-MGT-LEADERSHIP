# Management & Leadership Mid-Semester Report — Initiative

**Ahsan | Georgia Tech | Spring 2026**

---

## Describe your initiative/procedure.

My initiative is a comprehensive, plain-language reference guide that covers the full compute workflow for Georgia Tech researchers who have working code but little to no experience with HPC or cloud infrastructure. The guide walks a researcher from "I have code" to "it's running optimally on PACE or AWS." It spans profiling and bottleneck identification, resource right-sizing, a decision framework for PACE vs. AWS, end-to-end workflows for both platforms (Slurm job scripts, storage tiers, QoS levels on PACE; instance selection, Spot pricing, and billing safety on AWS), containerization and portability with Docker/Apptainer, and worked examples covering deep learning training, bioinformatics pipelines, and large-memory data processing. The target audience is PhD students, postdocs, and faculty—no prior knowledge of Slurm, AWS, or Docker is assumed.

## Explain the hypotheses/KPIs you have measured at this time and what is left to be measured.

The core hypothesis is that GT researchers waste compute resources (or lose work to crashed jobs) primarily because there is no single, accessible guide bridging the gap between "code that works" and "code running efficiently on real infrastructure." KPIs measured so far:

- **Content coverage:** Drafts are complete for the profiling, resource right-sizing, and PACE workflow sections. AWS workflow and containerization sections are in progress.
- **Technical accuracy:** Each completed section has been tested against real PACE job submissions to verify that instructions produce expected results.
- **Accessibility:** Early sections have been reviewed for clarity by a non-HPC peer to confirm the plain-language goal is being met.

Remaining KPIs include completing coverage of AWS and containerization sections, adding all worked examples, and conducting a broader usability review with target users before the end of the semester.

## Explain your method for testing these hypotheses via flowcharts.

The testing method follows a sequential pipeline:

1. Draft a section based on research and documentation review
2. Validate instructions by executing them on the actual platform (PACE or AWS)
3. Revise based on what breaks or confuses
4. Peer review for plain-language clarity
5. Integrate feedback and finalize

Each section cycles through steps 2–4 at least once before being considered complete. The worked examples at the end of the guide serve as an integration test—if a reader can follow them end-to-end using only the guide, the hypothesis is supported.

## Explain how stakeholders are engaging with your initiative. Reflect on whether their engagement matches your expectations and what changes may be necessary given the behavior that you observed.

The primary stakeholders are GT researchers who would use this guide and the PACE support team whose documentation I reference. Engagement so far has been limited to informal feedback from a small number of peers in my program who represent the target audience. Their engagement has matched expectations at this stage—the guide is still in active drafting, so broad outreach would be premature. One change I'm considering is reaching out to PACE support staff earlier than planned to ensure the guide aligns with any upcoming platform changes, rather than waiting until the final review stage.

## What processes have you documented or begun documenting to ensure the sustainability of your initiative? Where are you hosting this procedure? What additional documentation do you plan to complete?

The guide itself is the primary documentation artifact and is being developed in a dedicated Claude project, with version history maintained across sessions. The final deliverable will be a polished, shareable document. For sustainability, the guide is structured so individual sections (e.g., PACE workflow, AWS workflow) can be updated independently as platforms evolve, without requiring a full rewrite. Additional documentation I plan to complete includes a maintenance checklist noting which sections are most likely to need updates (e.g., AWS pricing, PACE QoS levels) and suggested review cadence.

## How are you currently measuring progress toward your goals? What indicators of success or challenges have you identified so far?

Progress is measured by section completion against the overall outline. At the midpoint, roughly half of the planned sections have complete drafts, with the remaining sections in various stages of research and drafting. A key indicator of success is that the completed sections pass the "execution test"—instructions actually work when followed on PACE. The primary challenge has been the depth required for the AWS section, where pricing models, instance families, and Spot market behavior require significantly more research than the PACE sections, which benefit from my direct experience with the platform.

## What obstacles or bottlenecks have you encountered in implementing your initiative? Which anticipated challenges have materialized, and what unexpected issues have arisen?

The anticipated challenge of scoping—deciding how deep to go on each topic without making the guide overwhelming—has materialized as expected. Balancing comprehensiveness with accessibility is a constant tension. An unexpected issue has been the difficulty of writing platform-agnostic containerization guidance; Docker and Apptainer have subtle behavioral differences that are hard to explain without getting into weeds that may lose the target audience. I've addressed this by focusing on the most common use cases rather than trying to cover every edge case.
