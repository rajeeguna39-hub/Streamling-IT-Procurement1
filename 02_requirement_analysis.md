# Phase 2 - Requirement Analysis

## Functional Requirements

### FR-01: Laptop Request

The system shall provide a standard laptop procurement request form.

### FR-02: Required Information

The request should capture: - Requested for - Department - Job role -
Laptop model/category - Business justification - Required date -
Location - Cost center - Manager

### FR-03: Validation

The system shall validate mandatory information before processing the
request.

### FR-04: Approval

The system shall route the request to the appropriate manager/approver.

### FR-05: Fulfillment

After approval, the system shall create the required
fulfillment/procurement tasks.

### FR-06: Notifications

The system shall notify relevant users when the request is submitted,
approved, rejected, dispatched, and completed.

### FR-07: Tracking

Users and IT staff shall be able to view the current request status.

### FR-08: Audit

Important actions and status changes shall be recorded for audit
purposes.

## Non-Functional Requirements

-   Secure access based on roles.
-   Simple and user-friendly request form.
-   Reliable workflow execution.
-   Traceable approvals.
-   Maintainable Flow Designer configuration.
-   Reasonable response time.

## Business Rules

1.  Mandatory fields must be completed.
2.  Requests must have an identified approver.
3.  Fulfillment should not begin before approval.
4.  Rejected requests should stop the normal fulfillment path.
5.  Exceptions should be routed to the appropriate support/procurement
    team.

## Inputs

-   Employee information
-   Laptop selection
-   Business justification
-   Delivery information
-   Approval information

## Outputs

-   Approved/rejected request
-   Fulfillment task
-   Procurement task where applicable
-   Status updates
-   Notifications
-   Completion record

## Acceptance Criteria

The workflow is acceptable when a standard laptop request can travel
from submission to completion while maintaining the required approvals,
tasks, notifications, and audit information.
