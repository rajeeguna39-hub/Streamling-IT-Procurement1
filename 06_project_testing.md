# Phase 6 - Project Testing

## Testing Objective

Verify that the standard laptop procurement workflow works correctly for
normal, rejected, incomplete, and exceptional requests.

## Test Cases

  -----------------------------------------------------------------------
  ID                      Test Case               Expected Result
  ----------------------- ----------------------- -----------------------
  TC-01                   Submit complete request Request is created
                                                  successfully

  TC-02                   Submit without required User is prompted to
                          field                   provide required data

  TC-03                   Manager approves        Fulfillment task is
                                                  created

  TC-04                   Manager rejects         Fulfillment does not
                                                  start and requester is
                                                  notified

  TC-05                   Verify assignment       Task is assigned to the
                                                  correct group

  TC-06                   Verify approval         Approver receives
                          notification            notification

  TC-07                   Verify approval result  Request status reflects
                                                  approval

  TC-08                   Complete fulfillment    Request moves to
                                                  completed state

  TC-09                   Verify completion       Requester receives
                          notification            completion message

  TC-10                   Stock unavailable       Exception path is
                                                  triggered

  TC-11                   Invalid approver        Request is routed for
                                                  correction/escalation

  TC-12                   Check audit history     Important actions are
                                                  traceable
  -----------------------------------------------------------------------

## User Acceptance Testing

A tester should: 1. Submit a standard laptop request. 2. Confirm all
required fields. 3. Approve the request as the manager. 4. Verify that
fulfillment is created. 5. Complete the fulfillment task. 6. Verify
request closure. 7. Verify all expected notifications.

## Defect Tracking

For each defect record: - Defect ID - Description - Steps to reproduce -
Expected result - Actual result - Severity - Status - Fix details -
Retest result

## Exit Criteria

Testing can be considered complete when critical workflow paths pass and
identified defects are resolved or formally accepted.
