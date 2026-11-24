# Product Requirements Document

> **Product name:** Working title to be decided  
> **Document status:** Draft / In progress  
> **Product stage:** Discovery and MVP definition  
> **Last updated:** 24 November 2026  
> **Research status:** Early exploratory responses collected; further validation required  
> **Audience:** Students in tertiary education across institutions and countries

## 1. Product Overview

### 1.1 Product summary
A student-focused planning application intended to help people manage academic work alongside the other responsibilities that compete for their time. The product concept brings tasks, deadlines, projects, commitments and opportunities into a clearer personal planning workflow.

The intended first release is deliberately narrow: help a student capture responsibilities, understand what needs attention, and keep important deadlines visible. The product should not assume that every student has the same workload, institution, calendar or internet access.

### 1.2 Product direction
The product will investigate whether students benefit from:
- A reliable place to capture tasks and commitments.
- A useful daily and upcoming view.
- Context for each task, such as project, area, due date, priority and estimated effort.
- A way to keep track of opportunities and their deadlines.
- Access to essential saved information when connectivity is limited.

These are product hypotheses to validate, not all confirmed MVP requirements.

## 2. Problem Statement

Students may coordinate classes, assignments, examinations, personal projects, employment, businesses, family responsibilities, clubs, volunteering and applications. Their planning information may be distributed across calendars, notes, chats, paper planners, task apps, browser tabs and memory.

This can create several possible difficulties:
- A student may not have one dependable overview of upcoming responsibilities.
- A task may be recorded without enough context to decide when to do it.
- A saved opportunity or message may not be revisited before its deadline.
- A student may know what needs doing but struggle to execute or prioritise it.
- A digital planning workflow may become less useful when internet access is unreliable.

**Problem hypothesis:** fragmented planning and weak follow-through can make it harder for some students to see, prioritise and complete their responsibilities.

**Evidence limitation:** the current survey is small and exploratory. It does not establish how common these problems are among students generally. Further interviews and a broader sample are required before treating this hypothesis as validated.

## 3. Business Objectives and Product Outcomes

### 3.1 Product objectives
1. Validate whether students need a more coherent way to manage academic and non-academic responsibilities.
2. Help users capture and retrieve tasks without unnecessary friction.
3. Make upcoming deadlines and priorities easier to understand.
4. Test whether organising work by project or life area improves planning.
5. Learn whether opportunity tracking and offline access are important enough for the initial release.

### 3.2 MVP outcomes to evaluate
- Users can add, edit and find a task without assistance.
- Users can identify what requires attention today and next.
- Users understand the context and status of their tasks.
- Users can maintain access to essential saved information during connectivity interruptions, if offline support is included in the MVP.
- Test users voluntarily return to the product during the evaluation period.

No adoption, retention or performance targets have been set yet. Baselines and target values must be agreed after usability testing.

## 4. Target Users

### 4.1 Primary audience
Students enrolled in tertiary education, including university, college and other post-secondary programmes. The product should be usable across institutions and countries rather than being designed around one campus.

### 4.2 Research segments to include
- Students whose main responsibility is coursework and examinations.
- Students balancing academics with employment or a business.
- Students involved in clubs, leadership, volunteering or community work.
- Students managing personal, creative or technical projects.
- Students applying for internships, scholarships, competitions or programmes.
- Students with family or caregiving responsibilities.
- Students with limited or inconsistent internet access.

These are research segments, not fixed personas. The team should avoid assuming that every student belongs to only one segment.

### 4.3 User needs to validate
- How users currently capture tasks and commitments.
- How they decide what to work on next.
- Which details they need when reviewing a task.
- How they track progress and unfinished work.
- How they save and revisit opportunities.
- What happens when their preferred tools or internet connection are unavailable.

## 5. Stakeholders

| Stakeholder | Interest / responsibility | Current status |
|---|---|---|
| Student users | Provide needs, workflows, feedback and usability evidence | Research participants |
| Product team | Define the problem, scope, priorities and product decisions | In progress |
| Design team | Translate validated needs into information architecture and interface flows | In progress |
| Frontend team | Implement user-facing screens, interactions and responsive behaviour | In progress |
| Backend team | Define data models, APIs, validation, authentication and persistence | In progress |
| Course instructor / assessor | Assess whether the team has followed the discovery and PRD requirements | Assignment stakeholder |
| Future operator / administrator | Potential responsibility for support, access and service maintenance | Role to be clarified |

No external client, institutional sponsor or formal business owner has been confirmed. The team should identify who owns product decisions and who approves changes to scope.

## 6. User Stories and Acceptance Criteria

### US-01: Capture a task
**As a student, I want to add a task quickly so that I do not have to rely on remembering it.**

Acceptance criteria:
- The user can create a task with a title.
- The user can optionally add a due date, area or project, priority and estimated effort if those fields are included in the agreed MVP.
- The system validates required fields and explains invalid input.
- A successfully saved task appears in the relevant task list.
- The user receives clear confirmation that the task was saved.

### US-02: Review today's work
**As a student, I want to see what needs attention today so that I can choose my next action.**

Acceptance criteria:
- The daily view displays tasks due today.
- Overdue tasks are distinguishable from tasks due later, if overdue handling is included.
- Each task displays enough information to identify it and understand its urgency.
- An empty state explains that there are no tasks in the selected view and provides a clear next action.

### US-03: See upcoming deadlines
**As a student, I want to review upcoming deadlines so that I can prepare before work becomes urgent.**

Acceptance criteria:
- The user can access a defined upcoming period.
- Tasks are ordered consistently by due date and time where available.
- Tasks without due dates are not silently presented as deadline-based items.
- The user can open a task to view its full details.

### US-04: Organise tasks by context
**As a student, I want to group tasks by project or area so that I can understand what each task belongs to.**

Acceptance criteria:
- A task can be associated with a defined area or project if this is included in the MVP.
- The user can view tasks within that context.
- A task's context is visible in its detail view and any list where it is needed to distinguish tasks.
- The team defines whether a task can belong to more than one project before implementation.

### US-05: Update task progress
**As a student, I want to mark a task's progress so that I can distinguish unfinished work from completed work.**

Acceptance criteria:
- The user can change a task's status using the agreed status model.
- The updated status is reflected wherever the task appears.
- The system prevents invalid status values.
- The team defines whether completed tasks can be reopened and how they are archived.

### US-06: Track an opportunity
**As a student, I want to save an opportunity and its deadline so that I can return to it before applications close.**

Acceptance criteria:
- The user can save an opportunity title.
- The user can add a source link and deadline.
- The user can update its application status.
- The user can find saved opportunities in a dedicated or clearly labelled view.
- The system handles missing or invalid links and dates clearly.

### US-07: Access saved information with poor connectivity
**As a student, I want to access essential saved information when my connection is unreliable so that I can still consult my plans.**

Acceptance criteria:
- The team explicitly documents which information is available offline.
- The interface indicates when the user is offline or changes are pending synchronisation.
- The system does not silently discard locally saved changes.
- The team defines conflict handling before claiming synchronisation is complete.

## 7. Functional Requirements

Priorities use MoSCoW: **Must** is essential to the first usable release; **Should** is important but can follow if necessary; **Could** is optional; **Won't (this release)** is explicitly excluded.

| ID | Requirement | Priority | Verification |
|---|---|---|---|
| FR-01 | The system shall allow a user to create an account and sign in. | Must | Register and sign-in tests |
| FR-02 | The system shall allow an authenticated user to create a task with a title. | Must | Create-task test |
| FR-03 | The system shall allow a user to view their own saved tasks. | Must | Task-list test |
| FR-04 | The system shall allow a user to edit a saved task. | Must | Edit-task test |
| FR-05 | The system shall allow a user to assign a due date to a task. | Must | Date validation test |
| FR-06 | The system shall provide a daily view of tasks requiring attention. | Must | Daily-view test |
| FR-07 | The system shall provide an upcoming-deadlines view for an agreed time window. | Must | Upcoming-view test |
| FR-08 | The system shall order deadline-based tasks consistently by due date/time. | Must | Sorting test |
| FR-09 | The system shall allow tasks to be grouped by area or project. | Should | Grouping and filtering test |
| FR-10 | The system shall allow users to update task status. | Should | Status transition test |
| FR-11 | The system shall allow users to save an opportunity title, link and deadline. | Should | Opportunity creation test |
| FR-12 | The system shall allow users to update an opportunity's application status. | Should | Status update test |
| FR-13 | The system shall provide access to saved information during connectivity interruptions. | Could; validate feasibility | Offline test plan |
| FR-14 | The system shall synchronise locally saved changes after reconnection, if offline editing is supported. | Could; depends on FR-13 | Sync and conflict tests |

The Must/Should/Could classification is a proposed starting point. The team must confirm it against implementation time, research evidence and the assignment scope.

## 8. Non-Functional Requirements

| Category | Requirement | How it will be evaluated |
|---|---|---|
| Usability | Core actions should be understandable without external instruction. | Observe representative users completing key tasks; record completion and confusion points. |
| Accessibility | Text, controls and feedback should remain perceivable and usable across common screen sizes and input methods. | Responsive and accessibility review. |
| Responsiveness | The interface should adapt to mobile and desktop viewports without losing essential functionality. | Test agreed viewport sizes. |
| Performance | Common screens and save actions should respond within an agreed target under defined test conditions. | Set numeric targets after the team chooses its environment and test method. |
| Reliability | A successful save should persist and remain available after the user returns. | Persistence and failure-recovery tests. |
| Security | Users must only access their own private tasks and account data. | Authentication and authorisation tests. |
| Privacy | Collect only information needed for the product; explain what is stored and why. | Data inventory and privacy review. |
| Compatibility | The product should support the agreed browsers and devices. | Define a supported-browser matrix and test it. |
| Connectivity resilience | The interface should communicate connection and sync state accurately. | Simulated offline and reconnection tests, if supported. |

Numeric service targets, supported browser versions, backup policy and availability targets remain open decisions. The team must not use vague claims such as “fast” or “secure” as final testable requirements.

## 9. Scope and Priorities

### 9.1 Proposed MVP
- Account creation and sign-in.
- Create, view and edit tasks.
- Task title and due date.
- Daily task view.
- Upcoming-deadlines view.
- Consistent deadline ordering.

### 9.2 Candidate features requiring validation
- Grouping by area or project.
- Task priority and estimated effort.
- Task status and progress.
- Opportunity tracker.
- Offline access and synchronisation.

### 9.3 Out of scope for the first release
- Social feed or public profiles.
- Payments and financial transactions.
- AI-generated schedules or recommendations.
- Shared team workspaces and collaboration.
- Complex calendar integrations.
- Automated opportunity discovery.

### 9.4 MVP decision rule
A feature should enter the MVP only if it addresses a validated user need, can be implemented and tested within the team's constraints, and is necessary for the first usable workflow. Features that are useful but not essential should be deferred.

## 10. Assumptions and Open Questions

### 10.1 Current assumptions
- Some students manage academic and non-academic responsibilities at the same time.
- Some students use several tools or manual methods to organise work.
- A daily and upcoming view may help users decide what to do next.
- Some users may value offline access.
- Opportunity tracking may be useful to a subset of students.

These assumptions are not yet established as universal or representative findings.

### 10.2 Open questions
1. Which student segment experiences the clearest unmet need?
2. Do users want one combined task list or separate views by area/project?
3. Which fields are essential when creating a task?
4. Do users think in terms of priority, urgency, estimated effort, deadlines, or a combination?
5. What does “progress” mean to users: not started/in progress/done, percentage complete, or smaller steps?
6. Is opportunity tracking essential to the first release or a later module?
7. What information must remain available offline?
8. Should users be able to edit offline, or only view previously saved information?
9. Which calendar or notification integrations do users expect?
10. What is the simplest product workflow that users would return to?

### 10.3 Risks
| Risk | Potential impact | Mitigation |
|---|---|---|
| Small or biased research sample | Product decisions may reflect only a narrow group | Recruit across institutions, countries and responsibility patterns |
| Feature expansion | MVP becomes too large to finish | Use MoSCoW and keep the first workflow narrow |
| Existing tools already solve the problem | Users may have little reason to switch | Investigate current workarounds and unmet needs |
| Offline sync complexity | Data conflicts or lost changes | Prototype and test a limited offline scope before promising full sync |
| Unclear product ownership | Conflicting requirements and rework | Assign a decision owner and record team decisions |

## 11. Research and Discovery Evidence

### 11.1 Method and limitations
An exploratory online questionnaire was distributed through Tally. The submission export currently contains **10 completed submissions**. One response is the team's known mock/test submission and is excluded from the descriptive summary below, leaving **9 preliminary non-test submissions**.

This is a small convenience sample, not a representative survey. The team has not verified that all respondents are unique or that the sample reflects students across countries and institutions. The findings are directional only. Some free-text responses are brief and need follow-up interviews.

### 11.2 Preliminary respondent profile
- 9 non-test submissions remain after excluding the known mock response.
- All 9 selected undergraduate / bachelor's study.
- 8 entered Nigeria and 1 entered India.
- The sample therefore does not yet provide meaningful coverage of different study levels or countries.

### 11.3 Descriptive patterns in the 9 preliminary responses
Multiple selections are counted separately, so totals may exceed the number of respondents.

| Area | Preliminary observation |
|---|---|
| Responsibilities | Personal/creative/technical projects and student clubs/leadership were each selected by 4 respondents. Family/home responsibilities were selected by 3. Two selected the option that study is their main commitment. |
| Planning tools | Messaging apps were selected by 5 respondents. Paper planners, notes apps and calendars were each selected by 3. Three also selected reliance on memory. |
| Opportunity handling | 3 respondents said they save a link/message and plan to revisit it later; 2 keep it in an open tab or try to remember it; 2 add it to a task list/calendar; 2 set a reminder or calendar deadline. |
| Connectivity | 3 said they switch to paper/screenshots/offline methods; 3 said they cannot access needed information until back online; 1 can view saved information but some features stop working; 1 reported no issue; 1 rarely uses digital organisation tools. |
| First information needed | 4 selected what they need to do today; 3 selected upcoming deadlines/appointments; 2 selected all tasks grouped by area/project. |

### 11.4 What these responses may suggest
- Messaging tools and manual methods appear in the current workflows represented in this small sample.
- Some respondents describe relying on memory, open tabs or saved messages to revisit tasks and opportunities.
- Daily tasks and upcoming deadlines were the most selected first-view needs in this sample.
- Connectivity interruptions may affect some respondents, but the responses do not establish how often this happens or whether offline editing is required.
- The opportunity-tracking responses are mixed; this feature should not automatically be treated as a Must-have.

### 11.5 Design implications to investigate
These are hypotheses for design exploration, not final decisions:
- Test a home screen that makes today's tasks and upcoming deadlines immediately visible.
- Compare a single combined task list with area/project grouping.
- Test task cards that show due date and priority together; some respondents also selected estimated effort, project context, progress or opportunity eligibility/deadline details.
- Explore a lightweight capture flow that works for users who currently rely on messages, notes or paper.
- Validate whether users need offline viewing only or offline editing and synchronisation.
- Treat reminders as a candidate workflow to test, not an assumed requirement.

### 11.6 Next research steps
1. Conduct follow-up interviews to understand what respondents mean by “executing the plans,” “not remembering on time,” and other brief answers.
2. Recruit students from more countries, study levels and institution types.
3. Include students with mostly academic workloads as well as those balancing work, projects and family responsibilities.
4. Ask participants to demonstrate how they currently capture a task and return to it later.
5. Validate the proposed dashboard and task-card information hierarchy with low-fidelity prototypes.
6. Update this section with interview dates, participant counts, anonymised evidence and any changes to the product decisions.

## 12. Success Measures

**Status: Not yet defined.** Establish baselines and targets after MVP usability testing.

Candidate measures:
- Task creation completion rate in usability tests.
- Time and error rate when users locate the next task due.
- Percentage of users who correctly identify their upcoming deadlines.
- Successful opportunity creation and status update, if included.
- Successful retrieval of saved information during connectivity interruption, if included.
- Repeat use during a defined pilot period.

Each metric needs a precise definition, measurement method, sample and target before it becomes a formal success criterion.

## 13. Dependencies and Implementation Considerations

- Frontend and backend teams must agree on task fields, status values, date/time handling and validation rules.
- The team must define authentication and user-data ownership before implementing private task records.
- The design team needs agreement on the primary navigation and the distinction between daily, upcoming, project and opportunity views.
- Offline support depends on an agreed local-storage and synchronisation strategy; it should not be promised until tested.
- The team should document API contracts and data-model decisions separately as implementation work progresses.

## 14. Current Project Status and Next Steps

**Current status: Discovery and MVP definition in progress.**

| Workstream | Current focus | Status |
|---|---|---|
| Product and research | Validate user problem and refine scope | Early survey collected; interviews still needed |
| Design | Information architecture, dashboard, task cards, empty states and onboarding | In progress |
| Frontend | Navigation, responsive layouts, task capture and editing flows | In progress |
| Backend | Data model, API contracts, authentication and persistence | In progress |
| Success measurement | Define usability and pilot metrics | Pending |

### Immediate next steps
1. Review the preliminary survey patterns with the team.
2. Conduct follow-up interviews and record evidence separately from assumptions.
3. Agree on the Must-have MVP workflow.
4. Have design produce low-fidelity wireframes for the daily view, upcoming view and task capture flow.
5. Have frontend and backend agree on task fields, status model, validation and API contracts.
6. Revisit the PRD after stakeholder feedback and implementation decisions.

---

## Document Maintenance

This PRD is a living document. Record the date and reason for material changes. Keep research observations, product decisions, assumptions and unresolved questions distinct. Do not report exploratory survey patterns as representative facts or proposed metrics as achieved results.
