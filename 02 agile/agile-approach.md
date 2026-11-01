## 1. Purpose

This document describes the Agile-inspired approach used to plan, develop, validate, and deliver the Digital Banking Financial Performance & Customer Profitability Analysis project.

The project will be completed independently using structured planning artifacts such as:

- Product backlog
- Epics and user stories
- Acceptance criteria
- Sprint planning
- Sprint goals and tasks
- Iterative reviews
- Testing and validation

The approach demonstrates how an analyst can organize an analytical project into manageable deliverables while maintaining alignment with business requirements.

## 2. Agile Delivery Principles

The project will follow these principles:

1. **Business value first:** Prioritize deliverables that answer the defined business questions.
2. **Incremental development:** Build the solution in manageable stages.
3. **Clear requirements:** Use documented requirements, user stories, and acceptance criteria.
4. **Continuous validation:** Validate SQL results and dashboard calculations throughout development.
5. **Transparency:** Maintain a visible backlog and document project progress.
6. **Adaptability:** Refine the analysis when findings or data limitations require changes.
7. **Traceability:** Connect business requirements to KPIs, SQL analysis, Power BI outputs, and testing.

## 3. Project Delivery Structure

The project will be organized into four planned sprints.

| Sprint | Focus | Key Deliverables |
|---|---|---|
| Sprint 1 | Initiation and Requirements | Project initiation document, BRD, stakeholder analysis, KPI catalog, backlog |
| Sprint 2 | Data Preparation and PostgreSQL | Data organization, database schema, data import, validation queries, initial SQL analysis |
| Sprint 3 | Financial Analysis and Power BI | Financial analysis, customer analysis, transaction analysis, Power BI data model and dashboard |
| Sprint 4 | Testing and Portfolio Delivery | Testing, reconciliation, recommendations, executive summary, GitHub documentation |

Each sprint will have a defined goal, tasks, and expected outputs.

## 4. Agile Roles and Responsibilities

Because this is an independent project, responsibilities are assigned for portfolio demonstration.

| Role | Responsibility |
|---|---|
| Business Analyst | Define business requirements, stakeholder needs, user stories, and acceptance criteria |
| Financial Analyst | Analyze revenue, operating costs, customer contribution, and financial KPIs |
| BI Analyst | Develop SQL queries, analytical models, and Power BI reporting |
| Product Owner — Simulated | Prioritize the backlog based on business value |
| Scrum Master — Simulated | Support planning, track progress, and identify blockers |
| Project Sponsor — Simulated | Review the final project outcomes and business recommendations |

The analyst may perform multiple responsibilities. These roles are not presented as actual separate team members.

## 5. Product Backlog Management

The project backlog will contain the work required to deliver the analytical solution.

Each backlog item will include:

- Unique backlog ID
- Epic
- User story or task description
- Priority
- Acceptance criteria
- Estimated effort
- Current status

Backlog items will be prioritized according to business value, dependencies, and project scope.

### Backlog Priority Definitions

| Priority | Definition |
|---|---|
| Must Have | Essential to answer the core business questions |
| Should Have | Important to improve analytical value or usability |
| Could Have | Useful enhancement if time permits |
| Won't Have — Current Scope | Excluded from the current project scope |

### Backlog Workflow

The planned workflow is:

`To Do → In Progress → Done`

A `Blocked` status may be used when work cannot proceed because of a dependency or unresolved issue.

## 6. Sprint Planning

At the beginning of each sprint, the following activities will be performed:

1. Review the project objective and relevant requirements.
2. Select backlog items for the sprint.
3. Confirm dependencies and expected outputs.
4. Define the sprint goal.
5. Break selected items into actionable tasks.
6. Establish acceptance criteria for completion.

Sprint scope may be adjusted if a dependency or data limitation affects delivery. Any material scope change will be documented.

## 7. Sprint Reviews

At the end of each sprint, the completed work will be reviewed against its goal.

The review will assess:

- Whether the expected deliverables are complete
- Whether the outputs meet their acceptance criteria
- Whether the work addresses the business requirements
- Whether any issues or limitations remain
- Whether the backlog requires updates

For this independent project, sprint reviews will be documented as self-reviews rather than meetings with actual stakeholders.

## 8. Retrospective Approach

After each sprint, a short retrospective will be completed.

The retrospective will consider:

| Area | Review Question |
|---|---|
| What went well? | Which activities or deliverables were effective? |
| What could improve? | What created unnecessary effort or confusion? |
| What was learned? | What new analytical or business knowledge was gained? |
| What will change? | What action should be applied in the next sprint? |

The retrospective will focus on improving the project workflow, analytical quality, and documentation.

## 9. Definition of Ready

A backlog item is considered ready for development when:

- The business purpose is understood.
- The required data or dependency is identified.
- The expected outcome is documented.
- Acceptance criteria are defined.
- The item is sufficiently clear to begin work.

## 10. Definition of Done

A backlog item is considered complete when:

- The agreed work has been implemented.
- Acceptance criteria have been met.
- Relevant calculations or outputs have been validated.
- Documentation has been updated.
- The deliverable is saved in the correct repository location.
- Any known limitations are documented.
- The item is marked as `Done` in the backlog.

For financial analysis, completion also requires that financial measures use **USD ($)** consistently and that revenue, transaction value, operating costs, and profitability are not incorrectly treated as interchangeable measures.

## 11. Tools

| Tool | Intended Use |
|---|---|
| Jira or Jira-style backlog | Track epics, user stories, tasks, priorities, and statuses |
| PostgreSQL | Store, query, and analyze project datasets |
| Power BI | Develop interactive financial and operational dashboards |
| GitHub | Store project files, SQL scripts, documentation, and deliverables |
| Markdown | Maintain project documentation |
| Excel | Retain the supplied raw data workbook and use only where necessary for data handling |

The project’s primary analytical focus will be PostgreSQL and Power BI.

## 12. Agile Artifacts

The following artifacts will be maintained within the repository:

| Artifact | Repository Location |
|---|---|
| Agile Approach | `project-management/agile/agile-approach.md` |
| Product Backlog | `project-management/agile/product-backlog.csv` |
| User Stories | `project-management/agile/user-stories.md` |
| Acceptance Criteria | `project-management/agile/acceptance-criteria.md` |
| Sprint Plan | `project-management/agile/sprint-plan.md` |
| Sprint 1 Tasks | `project-management/agile/sprint-1/sprint-1-goal-and-tasks.md` |
| Sprint 2 Tasks | `project-management/agile/sprint-2/sprint-2-goal-and-tasks.md` |
| Sprint 3 Tasks | `project-management/agile/sprint-3/sprint-3-goal-and-tasks.md` |
| Sprint 4 Tasks | `project-management/agile/sprint-4/sprint-4-goal-and-tasks.md` |

## 13. Conclusion

An Agile-inspired approach will help organize the project into clear, manageable deliverables.

The approach supports incremental development, requirements traceability, analytical validation, and continuous improvement while remaining transparent about the independent portfolio context.

The final solution will demonstrate a structured workflow from business requirements through PostgreSQL analysis, Power BI reporting, testing, and executive communication.
