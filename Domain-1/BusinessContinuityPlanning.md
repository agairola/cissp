## Planning for Business Continuity

*Business continuity planning (BCP)* involves assessing the risks to organizational processes and creating policies, plans, and procedures to minimize the impact those risks might have on the organization if they were to occur.

The `goal` of BCP planners is to implement a combination of policies, procedures, and processes such that a potentially disruptive event has as little impact on the business as possible. `mission-critical work tasks`

> BUSINESS CONTINUITY PLANNING VS. DISASTER RECOVERY PLANNING

> The distinction between the two is one of perspective. Both activities are designed to help prepare an organization for a disaster. They intend to keep operations running continuously, when possible, and recover operations as quickly as possible if they are disrupted. The perspective difference is that business continuity activities are typically strategically focused at a high level and center themselves on business processes and operations. Disaster recovery plans tend to be more tactical in nature and describe technical activities such as recovery sites, backups, and fault tolerance.

The BCP process has four main steps.

* Project scope and planning
* Business impact assessment
* Continuity planning
* Approval and implementation

## Project Scope and Planning

This requires the following:

* Structured `analysis of the business’s organization` from a crisis planning point of view
* The creation of a `BCP team` with the approval of senior management
* An `assessment of the resources available` to participate in business continuity activities
* An analysis of the `legal and regulatory` landscape that governs an organization’s response to a catastrophic event

### BUSINESS ORGANIZATION ANALYSIS

Perform an analysis of the business organization to identify all departments and individuals who have a stake in the BCP process. Here are some areas to consider:

* Operational departments that are responsible for the core services the business provides to its clients
* Critical support services, such as the information technology (IT) department, facilities and maintenance personnel, and other groups responsible for the upkeep of systems that support the operational departments
* Corporate security teams responsible for physical security, as they are many times the first responders to an incident and are also responsible for the physical safeguarding of the primary facility and alternate processing facility
* Senior executives and other key individuals essential for the ongoing viability of the organization

### BCP TEAM SELECTION

The team should include, at a minimum, the following individuals:

* `Representatives` from each of the organization’s departments responsible for the `core service`s performed by the business
* Business unit team `members from the functional areas` identified by the organizational analysis
* IT `subject-matter experts` with technical expertise in areas covered by the `BCP`
Cybersecurity team members with knowledge of the BCP process
* `Physical security` and facility management teams responsible for the physical plant
* `Attorneys` familiar with corporate legal, regulatory, and contractual responsibilities
* `Human resources` team members who can address `staffing issues` and the impact on individual employees
* `Public relations` team members who need to conduct similar planning for how they will communicate with stakeholders and the public in the event of a disruption
* `Senior management representatives` with the ability to set vision, define priorities, and allocate resources

### RESOURCE REQUIREMENTS

Team should perform assessment of the resources required by the BCP effort. This involves the resources required by three distinct BCP phases.

* Most important is people bandwidth 
* Testing, training, and maintenance phases of BCP
* During a disaster BCP team should be very caution when using its power to implement BCP as it would take almost all resources.

### LEGAL AND REGULATORY REQUIREMENTS

* Emergency services, such as police, fire, and emergency medical operations should also have solid BCP implementation. 
* Financial institutions, such as banks, brokerages, and the firms that process their data, are subject to strict government and international banking and securities regulations. 
* Pharmaceutical manufacturers 
* If your contracts include commitments to customers expressed as service-level agreements (SLAs), you might find yourself in breach of those contracts if a disaster interrupts your ability to service your clients
* On the flip side of the coin, a good BCP implementation can help your organization win new clients/customer.
* All of these concerns point to one conclusion—it’s essential to include your organization’s legal counsel in the BCP process.

## Business Impact Assessment

*Business impact assessment* (BIA) identifies the resources that are critical to an organization’s ongoing viability and the threats posed to those resources.

It’s important to realize that there are two different types of analyses that business planners use when facing a decision.

**Quantitative decision-making** Quantitative decision-making involves the use of numbers and formulas to reach a decision. This type of data often expresses options in terms of the dollar value to the business.

**Qualitative decision-making** Qualitative decision-making takes non-numerical factors, such as reputation, investor/customer confidence, workforce stability, and other concerns, into account. This type of data often results in categories of prioritization (such as high, medium, and low).

A good plan = Quantitative + Qualitative

```
Pretty good link: https://defaultreasoning.com/2013/12/10/rpo-rto-wrt-mtdwth/
```
### IDENTIFY PRIORITIES

* The priority identification task, or criticality prioritization, involves creating a comprehensive list of business processes and ranking them in order of importance.

* Be sure to gather input from all parts of the organization, even if some areas are not included on the team.

* *Asset value (AV)* 

* *Maximum tolerable downtime (MTD)*, sometimes also known as *maximum tolerable outage (MTO)*. The MTD is the maximum length of time a business function can be inoperable without causing irreparable harm to the business. 

* *Recovery time objective (RTO)* This is the amount of time in which you think you can feasibly recover the function in the event of a disruption. 

The goal of the BCP process is to ensure that your RTOs are less than your MTDs.

### RISK IDENTIFICATION

Risks come in two forms: natural risks and man-made risks. The following list includes some events that pose natural threats:

  * Violent storms/hurricanes/tornadoes/blizzards
  * Lightning strikes
  * Earthquakes
  * Mudslides/avalanches
  * Volcanic eruptions

Man-made threats include the following events:

  * Terrorist acts/wars/civil unrest
  * Theft/vandalism
  * Fires/explosions
  * Prolonged power outages
  * Building collapses
  * Transportation failures
  * Internet disruptions
  * Service provider outages

> Keep in mind that there are three different versions of the SOC report. The simplest of these, an SOC-1 report, covers only internal controls over financial reporting. If you want to verify the security, privacy, and availability controls, you’ll want to review either an SOC-2 or SOC-3 report. The American Institute of Certified Public Accountants (AICPA) sets and maintains the standards surrounding these reports to maintain consistency between auditors from different accounting firms.

### LIKELIHOOD ASSESSMENT

*  This assessment is usually expressed in terms of an *annualized rate of occurrence (ARO)* that reflects the number of times a business expects to experience a given disaster each year.

* The BCP team should sit down and determine an ARO for each risk identified in the previous section. These numbers should be based on corporate history, professional experience of team members, and advice from experts, such as meteorologists, seismologists, fire prevention professionals, and other consultants, as needed.

* Some government sources are - U.S. Geological Survey (USGS) for earthquakes, Federal Emergency Management Agency (FEMA) for flood

### IMPACT ASSESSMENT

* From a quantitative point of view, we will cover three specific metrics: the `exposure factor`, the `single loss expectancy`, and the` annualized loss expectancy`. Each one of these values is computed for each specific risk/asset combination evaluated during the previous phases.

* *Exposure factor (EF)* is the amount of damage that the risk poses to the asset, expressed as a percentage of the asset’s value.

* *Single loss expectancy (SLE)* is the monetary loss that is expected each time the risk materializes. You can compute the SLE using the following formula:

```
SLE = AV x EF
```

* *Annualized loss expectancy (ALE)* is the monetary loss that the business expects to occur as a result of the risk harming the asset over the course of a year. You already have all the data necessary to perform this calculation. The SLE is the amount of damage you expect each time a disaster strikes, and the ARO (from the likelihood analysis) is the number of times you expect a disaster to occur each year. You compute the ALE by simply multiplying those two numbers:

```
ALE = SLE x ARO
```

* From a qualitative point of view, you must consider the nonmonetary impact that interruptions might have on your business. For example, you might want to consider the following:

  * Loss of goodwill among your client base
  * Loss of employees to other jobs after prolonged downtime
  * Social/ethical responsibilities to the community
  * Negative publicity

### RESOURCE PRIORITIZATION

* From a quantitative point of view, this process is relatively straightforward. You simply create a list of all the risks you analyzed during the BIA process and sort them in descending order according to the ALE computed during the impact assessment phase. This provides you with a prioritized list of the risks that you should address. 

* Better would be to combine list for both quantitative and qualitative with BCP team and representatives from the senior management team.

## Continuity Planning

The next phase of BCP development, continuity planning, focuses on developing and implementing a continuity strategy to minimize the impact realized risks might have on protected assets.

In this section, you’ll learn about the subtasks involved in continuity planning.

  * Strategy development
  * Provisions and processes
  * Plan approval
  * Plan implementation
  * Training and education

### STRATEGY DEVELOPMENT

* Most accepted policy development would be to consider zero-downtime posture in the face of every possible risk but in real world its hard to achieve. 

* The BCP team should look back to the `MTD` estimates created during the early stages of the BIA and determine which risks are deemed `acceptable` and which must be mitigated by BCP continuity provisions. 

### PROVISIONS AND PROCESSES

* BCP team designs the specific procedures and mechanisms that will mitigate the risks deemed unacceptable during the strategy development stage.

* Three categories of assets must be protected through BCP provisions and processes: people, buildings/facilities, and infrastructure. 

#### People

* First, you must ensure that the people within your organization are safe before, during, and after an emergency. Once you’ve achieved that goal, you must make provisions to allow your employees to conduct both their BCP and operational tasks in as normal a manner as possible given the circumstances.

* Arrangements must be made for shelter and food if need be.

#### Buildings and Facilities

When you perform your BIA, you will identify those facilities that play a critical role in your organization’s continued viability. Your continuity plan should address two areas for each critical facility.

**Hardening Provisions**  mechanisms and procedures that can be put in place to protect your existing facilities against the risks defined in the strategy development phase.

**Alternate Sites**  not feasible to harden a facility against a risk, your BCP should identify alternate sites 

#### Infrastructure

* Every business depends on some sort of infrastructure for its critical processes - IT backbone of communications and computer systems that process orders, manage the supply chain, handle customer interaction, and perform other business functions. 

* The BCP must address how these systems will be protected against risks identified during the strategy development phase.

* As with buildings and facilities, there are two main methods of providing this protection.

**Physically Hardening Systems** example - computer-safe fire suppression systems and uninterruptible power supplies.
**Alternative Systems** example - introducing redundancy 

## Plan Approval and Implementation

Once the BCP team completes the design phase of the BCP document, it’s time to gain top-level management endorsement of the plan.

>  Senior management approval and buy-in is essential to the success of the overall BCP effort.


### PLAN APPROVAL

This move demonstrates the importance of the plan to the entire organization and showcases the business leader’s commitment to business continuity. The signature of such an individual on the plan also gives it much greater weight and credibility in the eyes of other senior managers, who might otherwise brush it off as a necessary but trivial IT initiative.

### PLAN IMPLEMENTATION

The BCP team should get together and develop an implementation schedule that utilizes the resources dedicated to the program to achieve the stated process and provision goals in as prompt a manner as possible given the scope of the modifications and the organizational climate.

### TRAINING AND EDUCATION

All personnel who will be involved in the plan (either directly or indirectly) should receive some sort of training on the overall plan and their individual responsibilities.

Everyone in the organization should receive at least a plan overview briefing.

People with direct BCP responsibilities should be trained and evaluated on their specific BCP tasks to ensure that they are able to complete them efficiently when disaster strikes. At least one backup person should be trained for every BCP task to ensure redundancy. 

### BCP DOCUMENTATION

Committing your BCP methodology to paper provides several important benefits:

* Document to reference in the event of an emergency, if the BCP member is not present
* `Historical record` of the BCP process that will be useful to future personnel seeking to both understand the reasoning behind various procedures and implement necessary changes in the plan.
* It forces the team members to commit their thoughts to paper and “sanity check.”

Important components of the written business continuity plan:

#### Continuity Planning Goals

* The plan should describe the goals of continuity planning as set forth by the BCP team and senior management.
* The most common goal of the BCP is quite simple: to ensure the continuous operation of the business in the face of an emergency situation.

#### Statement of Importance

* Reflects the criticality of the BCP to the organization’s continued viability.
* Signature of CEO come into play and would carry weright while implementing the plan. 

#### Statement of Priorities

*  Listing the functions considered critical to continued business operations in a prioritized order. 

#### Statement of Organizational Responsibility

* Comes from a senior-level executive and can be incorporated into the same letter as the statement of importance. 
* It basically echoes the sentiment that “business continuity is everyone’s responsibility!”

#### Statement of Urgency and Timing

* Expresses the criticality of implementing the BCP and outlines the implementation timetable decided on by the BCP team and agreed to by upper management. 

#### Risk Assessment

* Include a discussion of all the risks considered during the BIA as well as the quantitative and qualitative analyses performed to assess these risks. For the quantitative analysis, the actual AV, EF, ARO, SLE, and ALE figures should be included. For the qualitative analysis, the thought process behind the risk analysis should be provided to the reader.

#### Risk Acceptance/Mitigation

It should cover each risk identified in the risk analysis portion of the document and outline one of two thought processes:

* acceptable risk and reconsideration them in future
* unacceptable risk and  processes put into place to reduce the risk to the organization’s continued viability.

#### Vital Records Program

* This document states where critical business records will be stored and the procedures for making and storing backup copies of those records.

#### Emergency-Response Guidelines

The emergency-response guidelines outline the organizational and individual responsibilities for immediate response to an emergency situation. 

These guidelines should include the following:

* Immediate response procedures (security and safety procedures, fire suppression procedures, notification of appropriate emergency-response agencies, etc.)
* A list of the individuals who should be notified of the incident (executives, BCP team members, etc.)
* Secondary response procedures that first responders should take while waiting for the BCP team to assemble

#### Maintenance

* The BCP team should not be disbanded after the plan is developed but should still meet periodically to discuss the plan and review the results of plan tests to ensure that it continues to meet organizational needs.

* Minor changes to the plan do not require conducting the full BCP development process from scratch; they can simply be made at an informal meeting of the BCP team by unanimous consent

* Any time you make a change to the BCP, you must practice good version control. All older versions of the BCP should be physically destroyed and replaced by the most current version so that no confusion exists as to the correct implementation of the BCP.

#### Testing and Exercises

The BCP documentation should also outline a formalized exercise program to ensure that the plan remains current and that all personnel are adequately trained to perform their duties in the event of a disaster.