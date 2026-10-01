# Phase 5 - Project Development

## Development Environment

Use a ServiceNow development/personal developer instance.

## Step 1 - Create the Catalog Item

Create a catalog item such as:

**Name:** Standard Laptop Procurement

Add the required variables for employee, laptop type, justification,
delivery details, and approval information.

## Step 2 - Configure Variables

Example variables: - Requested for - Laptop type - Department - Business
justification - Required date - Delivery location - Cost center -
Manager

Mark required variables as mandatory.

## Step 3 - Create the Flow

Open **Flow Designer** and create a flow for the standard laptop
procurement request.

### Suggested Flow

**Trigger:** Catalog request / requested item is created.

**Actions:** 1. Get request information. 2. Validate mandatory
information. 3. Determine manager. 4. Ask for approval. 5. Use an
If/Else branch for approval result. 6. If rejected: - Update request
status. - Add rejection details. - Notify requester. 7. If approved: -
Create fulfillment task. - Assign task to IT/procurement. - Update
request status. - Notify requester. 8. Wait for fulfillment completion.
9. Update request to completed. 10. Send final notification.

## Step 4 - Configure Assignment

Assign tasks to the correct group, for example: - IT Service Desk -
Hardware Procurement - Asset Management

Use the groups available in the target ServiceNow instance.

## Step 5 - Configure Notifications

Create notifications for: - Request submitted - Approval requested -
Request approved - Request rejected - Fulfillment started - Request
completed

## Step 6 - Add Logging / Audit Information

Record important status changes, approval results, task assignments, and
completion information.

## Development Deliverables

-   Catalog item
-   Catalog variables
-   Flow Designer flow
-   Approval configuration
-   Fulfillment tasks
-   Notifications
-   Roles/access configuration
