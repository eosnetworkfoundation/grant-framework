# Workflow Description
The Grant Framework workflow allows the Grant Operations team to automatically:
- move grant applications though their states
- add them to a central spreadsheet for Ops management
- send emails to applicants at the appropriate steps

The first step in the overall grant workflow is the Pull Request.  A `pull_request_target` action sends the applicant an email to let them know the grant
was received and that it will go through processing.  The remainder of the workflow occurs when the grant operations team adds labels to that PR.

**Labels:**
- Grant Issues
- Grant Received
- Grant Translated
- Grant Committee Approved
- Grant Fully Approved
- Grant Rejected

## Upon Receipt of a Pull Request
When a pull_request is received in the grant-framework directory, the grant is parsed and a thank you email is sent to the applicant.

## Grant Issues
The grant has some formatting errors that will break the parser. Or it has incorrect information such as an invalid EOS Account name.
This label is applied, but the grant applicant must still be notified of the errors that need to be corrected.  It currently does
not send an email or do any workflow. `FUTURE:` it may send a generic email notifying the applicant that the grant needs some corrections.
It would cc the grants email address.  Then a simple reply all email can be send from that account to note the items that need to be addressed.

## Grant Received
This currnet does nothing but add the tag so it is clear the grant is valid and has been processed (and sent to be translated).

## Grant Translated
This adds the grant to the grant spreadsheet for the Grant Committee.  `FUTURE:` It should also sent the notification email to the Grant Committee
that there are new grants to be reviewed.

## Grant Committee Approved
This label sends an email to the applicant letting them know the first step of approval is completed and to look for feedback from the 
grant evaluators.

## Grant Fully Approved
This label sends an email to the applicant letting them know that the grant is fully approved and that they can begin coding.  It let's them 
know to work with the grant-milestones repo to report milestones and request payment.

## Grant Rejected
This tag currently does nothing.  `FUTURE:` This should send a rejection email and cc the grants email account.  Operations can then reply all to 
that email and list the reasons for rejection.

# Testing
There are a number of testing scripts that can call some of the reusable components.  They all begin with the word "test-" in this directory


![](https://img.shields.io/static/v1?label=&message=Ted%20Cahall&color=black&style=for-the-badge)

