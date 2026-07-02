IT Service Desk — Ticket Lifecycle Management (Jira)

Hands-on lab simulating first-level (N1) IT support ticket management using Jira.
This project demonstrates the full ticket lifecycle: intake, categorization, prioritization,
assignment, status tracking, documentation, and resolution — the core daily workflow of a
Help Desk / Service Desk analyst.

Objective

Reproduce a realistic Service Desk board and manage a set of common support tickets
end to end, distinguishing incidents (something broke) from service requests
(a standard ask), and documenting each case so any technician could pick it up.

Tools


Jira (Cloud) — Kanban board with workflow states.
Ticket types: Incident and Task (service request).
Workflow: To Do → In Progress → Waiting for Customer → Resolved.


Board overview

A Kanban board (Soporte IT) with a full Service Desk flow:


Resolved (4): incidents handled and documented.
Waiting for Customer (1): request paused pending third-party input.


Mostrar imagen

Tickets

IDSummaryTypePriorityFinal statusKAN-6Password reset / locked account (Active Directory)IncidentMediumResolvedKAN-5User cannot access email (Outlook / Office 365)IncidentLowResolvedKAN-7Network printer not printingIncidentMediumResolvedKAN-9PC with no internet accessIncidentMediumResolvedKAN-8New user onboarding (account provisioning)Task (request)LowWaiting for Customer

Incident vs. Service Request

A key Service Desk distinction demonstrated in this board:


Incident — an unplanned interruption (something is broken). KAN-5/6/7/9.
Service Request — a standard, planned ask (e.g. onboarding a new user). KAN-8.


This matters for prioritization and SLA handling.

Sample case — KAN-9 (network troubleshooting)

The internet-access incident documents a layer-by-layer network diagnostic, showing
structured troubleshooting rather than trial and error:


ipconfig /all → detected an APIPA address (169.254.x.x): the host failed to obtain
an IP from DHCP.
ipconfig /release + ipconfig /renew → host obtained a valid IP.
ping 8.8.8.8 → confirmed external connectivity.
nslookup → confirmed name resolution (DNS OK).
User confirmed connectivity restored.


Mostrar imagen

Ticket documentation standard

Every ticket tells a complete story:


Description — the original problem (symptom, since when, scope), written at intake.
Comments — the work performed and the final resolution.


Mostrar imagen

Service Desk metrics

The project summary provides an at-a-glance view of the queue: resolved vs. pending
tickets, priority breakdown, and work-type distribution — the kind of reporting a Service
Desk relies on to track its workload.

Mostrar imagen

Skills demonstrated


Ticket lifecycle management in Jira (intake → resolution).
Incident vs. service request categorization.
Prioritization and workflow state management.
Clear, reproducible ticket documentation.
Structured network troubleshooting (DHCP / connectivity / DNS).



Part of my IT Support / SysAdmin portfolio.
