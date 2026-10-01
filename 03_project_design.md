# Phase 3 - Project Design

## Solution Architecture

``` text
User
  |
  v
ServiceNow Catalog Item
  |
  v
Laptop Procurement Request
  |
  v
Flow Designer
  |
  +--> Validate Request
  |
  +--> Manager Approval
  |       |
  |       +--> Rejected -> Notify Requester -> End
  |
  +--> Approved
          |
          +--> Create Fulfillment Task
          |
          +--> Procurement / Asset Task
          |
          +--> Update Status
          |
          +--> Notify Requester
          |
          v
       Completed
```

## Proposed ServiceNow Components

-   Service Catalog Item
-   Variables / Variable Sets
-   Flow Designer Flow
-   Approval Action
-   Task creation
-   Notifications
-   Assignment groups
-   Request / Requested Item records
-   Reporting

## Suggested Request Variables

  Variable                 Type               Required
  ------------------------ ------------------ ----------
  Requested for            Reference          Yes
  Department               Reference/Choice   Yes
  Laptop type              Choice             Yes
  Business justification   Multi-line text    Yes
  Required date            Date               Yes
  Delivery location        String/Choice      Yes
  Cost center              String/Reference   Yes
  Manager                  Reference          Yes

## Flow Design

### Trigger

When a standard laptop procurement request is submitted.

### Actions

1.  Validate required information.
2.  Determine manager/approver.
3.  Ask for approval.
4.  If rejected, update status and notify requester.
5.  If approved, create fulfillment task.
6.  Assign task to the correct group.
7.  Update request status.
8.  Send progress notifications.
9.  When fulfillment is complete, close the request.
10. Send completion notification.

## Exception Handling

-   Missing manager -\> route to IT/procurement support.
-   Invalid request -\> return for correction.
-   Approval rejected -\> stop fulfillment.
-   Stock unavailable -\> notify procurement and requester.
-   Fulfillment failure -\> create escalation task.

## Security Design

Only authorized users should be able to create, approve, process, or
administer procurement requests according to their roles.
