# Gbagbe Product Requirements Document (PRD)

> **Document status:** Draft / In progress  
> **Product status:** In discovery and implementation planning  
> **Last updated:** 23 November 2026  
> **Research status:** Pending student interviews and validation

## 1. Product Overview

Gbagbe is a student productivity application intended to help Babcock University students keep their academic responsibilities, businesses, personal projects, and opportunities in one place so that important tasks and deadlines are less likely to be forgotten.

The first version will focus on a small set of practical tools: task management, a simple view of what is due, and an opportunity tracker. The product direction and requirements will be refined as the team gathers feedback from students and reviews implementation constraints.

## 2. Problem Statement

Students may have responsibilities outside lectures, including businesses, personal projects, volunteering, competitions, internships, scholarships, and other opportunities. These responsibilities can be tracked across different places such as WhatsApp, notes applications, calendars, phone reminders, and memory.

When information is scattered, it may be difficult to see what needs attention, keep track of deadlines, or remember to follow up on an opportunity.

**Validation note:** This is the problem hypothesis guiding the project. The team has not yet completed enough student research to present it as a confirmed finding. Interview examples, frequency, and the extent of the problem will be added after research.

## 3. Target Users

### Primary users
Babcock University students who manage responsibilities beyond their academic timetable, such as a business, personal projects, volunteering, or applications to opportunities.

### Secondary users
Students who mainly need help organising academic tasks and deadlines.

### User context to validate
- Which tools students currently use to track responsibilities.
- Whether students experience difficulty managing academic and non-academic commitments together.
- How students currently discover, save, and track opportunities.
- How unreliable internet access affects their use of productivity tools.
- Which features would be genuinely useful enough to become part of a student's routine.

## 4. Research and Discovery

Research is ongoing. The team intends to speak directly with students rather than rely only on assumptions or form responses.

### Research methods
- Short, conversational interviews with Babcock students.
- Review of existing productivity and planning applications.
- Collection of examples of current student workflows and difficulties.

### Interview coverage
The team should include students with different levels, departments, and responsibility patterns, including students who focus mainly on academics. This will help avoid designing only around the experiences of students who already manage several extracurricular commitments.

### Findings
**Pending research.** Add anonymised observations and direct examples after interviews have been conducted.

| Research item | Status | Notes |
|---|---|---|
| Student interviews | Pending | Add participant count and date range after completion |
| Current tools and workarounds | Pending | Record tools students actually mention |
| Common difficulties | Pending | Do not infer frequency before reviewing responses |
| Opportunity-tracking habits | Pending | Add observed patterns and examples |
| Internet/connectivity constraints | Pending | Record how often and how this affects users |

### Research evidence to add
For each useful finding, record the anonymised participant reference, the relevant observation or short quote, and what it means for the product. Do not include identifiable personal information.

## 5. Existing Alternatives

Students may already use a combination of:
- Google Calendar
- Notion
- WhatsApp saved messages or chats
- Phone reminders
- Notes applications

These are alternatives to investigate, not evidence that students use all of them or that they are inadequate. Interviews should establish which tools students actually use, what works for them, and where gaps remain.

The team is also reviewing the following products for interaction and design inspiration:
- Structured
- Todoist
- TickTick
- Notion
- Sunsama
- Motion

The purpose of this review is to understand useful patterns in navigation, task organisation, daily planning, focus, and scheduling. Gbagbe should develop its own interface and workflow rather than reproduce another product's screens.

## 6. Product Goals

The first version should aim to help a student:

1. See the tasks and responsibilities that need attention today and during the coming week.
2. Keep track of opportunities and their application deadlines.
3. Organise responsibilities by area, such as Academics, Business, Personal, and Opportunities.
4. Retain access to relevant task information when internet connectivity is poor, with changes synchronising when connectivity returns.

These goals will be reviewed after student research and MVP testing.

## 7. Non-Goals for Version 1

The first version will not include:
- Social networking or a public activity feed.
- Payments or financial transactions.
- AI-powered planning or recommendations.
- Group collaboration and shared workspaces.

These items may be reconsidered later if user research establishes a clear need.

## 8. MVP Scope

### 8.1 Account access
Users should be able to create an account and sign in.

### 8.2 Task management
Users should be able to:
- Create a task with a title and deadline.
- Assign a task to an area: Academics, Business, Personal, or Opportunities.
- Edit task details.
- View their tasks.

### 8.3 Opportunity tracking
Users should be able to save an opportunity with:
- Opportunity title.
- Relevant link.
- Application deadline.
- Application status.

The initial statuses will be:
- Saved
- Applying
- Submitted

### 8.4 Today view
Users should have a view of tasks due today and during the coming week. Tasks should be ordered by deadline so that nearer deadlines are visible first.

### 8.5 Connectivity
The product direction is to support local access to saved task information and synchronisation when the user reconnects. The exact offline behaviour, conflict handling, and technical approach still need to be specified during implementation planning.

## 9. User Stories and Acceptance Criteria

### Account access
**User story:** As a student, I want to create an account and sign in so that I can access my saved responsibilities.

**Acceptance criteria:**
- A user can submit valid registration details.
- A user can sign in with valid credentials.
- Invalid or incomplete input produces a clear error.
- Account and authentication details are handled securely.

### Create and organise a task
**User story:** As a student, I want to create a task and assign it to an area so that my responsibilities are organised.

**Acceptance criteria:**
- A task can be created with a title.
- A task can have a deadline.
- A task can be assigned to one of the defined areas.
- The new task appears in the user's task list.
- A user can edit an existing task.

### Track an opportunity
**User story:** As a student, I want to save an opportunity and track its application status so that I can follow the process.

**Acceptance criteria:**
- A user can save an opportunity with a title.
- A user can add a link and deadline.
- A user can set or update its status to Saved, Applying, or Submitted.
- Saved opportunities are available in the user's opportunity list.

### View upcoming responsibilities
**User story:** As a student, I want to see what is due today and this week so that I can decide what needs my attention.

**Acceptance criteria:**
- The Today view displays tasks due today.
- The view also makes tasks due during the coming week accessible.
- Tasks are ordered by deadline.
- An empty state is shown when there are no tasks in the selected period.

### Access information with limited connectivity
**User story:** As a student, I want to access saved task information when my connection is unreliable so that I can still refer to my plans.

**Acceptance criteria:**
- The intended offline data available to the user is documented before implementation is considered complete.
- Locally saved changes are retained while offline.
- Pending changes synchronise after connectivity returns.
- The user receives a clear indication when information has not yet synchronised.

**Implementation note:** These criteria describe the intended experience. The team must validate the technical approach and define behaviour for conflicting edits before treating offline support as complete.

## 10. Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Users can create an account and sign in. | MVP |
| FR-02 | Users can create and edit tasks. | MVP |
| FR-03 | Tasks can be assigned to Academics, Business, Personal, or Opportunities. | MVP |
| FR-04 | Tasks can have deadlines. | MVP |
| FR-05 | Users can save opportunities with a title, link, and deadline. | MVP |
| FR-06 | Opportunity status can be Saved, Applying, or Submitted. | MVP |
| FR-07 | Users can view tasks due today and during the coming week. | MVP |
| FR-08 | Tasks in the relevant view are ordered by deadline. | MVP |
| FR-09 | Saved task information should be accessible with limited or no connectivity. | MVP target; implementation details pending |

## 11. Non-Functional Requirements

- **Usability:** Core actions such as adding a task and checking upcoming deadlines should be straightforward.
- **Responsiveness:** The interface should work on mobile-sized screens as well as larger screens.
- **Performance:** Common views and actions should respond promptly under normal usage conditions.
- **Reliability:** User data should be stored consistently, and synchronisation failures should not silently discard changes.
- **Security:** Authentication and user data must be protected. Users should only be able to access their own private records.
- **Connectivity resilience:** The application should communicate its connection and synchronisation state clearly.

Specific measurable performance, availability, and security targets remain to be agreed during implementation.

## 12. Success Measures

**Status: Not yet defined.**

The team will establish measurable success criteria after the MVP scope is validated and a test group has used the product. Possible measures to consider include:
- Whether users can successfully create, edit, and find tasks.
- Whether users can save and update an opportunity.
- Whether users can identify what is due today and during the coming week.
- Whether users can retrieve saved information during a connectivity interruption.
- Whether users choose to keep using the product after initial testing.

No targets or results are being claimed at this stage. Baselines, measurement methods, and target values will be added after testing.

## 13. Risks and Open Questions

| Risk or question | Why it matters | Next step |
|---|---|---|
| The problem hypothesis may not represent most target users. | The team could build features students do not need. | Interview students with varied routines and responsibilities. |
| The MVP may become too broad. | Too many features could delay a usable first release. | Keep the initial scope focused on tasks, opportunities, and the Today view. |
| Offline support may add technical complexity. | Local data and server data must remain consistent. | Define offline behaviour and synchronisation rules before implementation. |
| Existing tools may already meet users' needs. | Students may have little reason to switch. | Understand current workflows and specific unmet needs. |
| Opportunity information may become outdated. | Saved links and deadlines can change. | Consider how users will review and update saved information. |

### Questions to resolve
- Which user group should the first test build prioritise?
- What task fields are essential and which can wait?
- What should happen when two versions of a task have changed before synchronisation?
- Should completed tasks remain visible, and for how long?
- What is the simplest useful offline experience for the first release?
- Which success measures can be collected responsibly during MVP testing?

## 14. Future Considerations

The following ideas are outside the current MVP and should only be prioritised after the core experience has been tested:
- Notifications and reminders.
- Timetable planning.
- Document storage for applications.
- Warnings or prompts when a user has taken on too many responsibilities.

## 15. Current Project Status and Next Steps

**Current status: In progress.** Gbagbe is at the discovery and implementation-planning stage. The PRD is a working document and should change as the team receives student feedback and confirms technical decisions.

| Workstream | Current focus | Status |
|---|---|---|
| Product and research | Conduct student interviews and validate the problem | Pending |
| Frontend | Review reference products and propose navigation, task views, and add/edit flows | In progress |
| Design | Explore visual directions, dashboard, timeline, empty states, and onboarding | In progress |
| Backend | Define data structure, API endpoints, and server organisation | In progress |
| Success measurement | Agree on MVP test criteria and measurable targets | Pending |

### Immediate next steps
1. Conduct short interviews with students from different departments and levels.
2. Summarise recurring observations without presenting assumptions as findings.
3. Review the frontend, design, and backend recommendations from the team.
4. Confirm the MVP requirements and technical decisions.
5. Update this PRD before using it as the final implementation reference.

---

## Document Maintenance

This document is expected to evolve. Replace pending sections with verified research, decisions, and test results as they become available. Keep unvalidated assumptions clearly labelled, and do not report proposed success measures as achieved outcomes.
