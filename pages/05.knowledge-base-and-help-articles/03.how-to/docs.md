---
title: 'How To'
media_order: '2018-03-24_11h02_47.png,2018-03-24_11h07_46.png,2018-03-24_11h11_06.png'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: true
visible: true
---

# How can I get an invoice / payment receipt for my eDoc Organizer Cloud Service subscription?

eDoc Organizer Cloud service is a monthly subscription document management service. Each month your credit card is charged automatically. You can print out the payment receipts for these charges directly from the eDoc Organizer Cloud service website. After you log into your eDoc Organizer Cloud service account at [https://cloud.edocorganizer.com/](https://cloud.edocorganizer.com/) follow the steps below to locate and print out the payment receipts.

1. Go to Account > Settings menu and click the 'Billing Statements' link under the Billing Information section.


2. On the Past Billing Statements page locate the payment that you want to print a receipt for and click the 'Payment Receipt' link in that row.


3. This will show you a payment receipt for the selected transaction. This page can be printed for your records or to be submitted to your accounting department.

# How do I make changes to my eDoc Organizer Cloud sevice plan?

You can change your subscription plan that defines the amount or space or number of users in your account at anytime. 

After you log into your eDoc Organizer Cloud service account at [https://cloud.edocorganizer.com/](https://cloud.edocorganizer.com/) follow the steps below to modify your subscription plan.

1. Go to Account > Settings menu and click the 'Change plan' link under the Current Subscription section.

2. Click the 'Email Security Code' button to receive a temporary security code to proceed with the change.

3. You will receive an email with a temporary security code that will allow you to change the plan on your account. 

4. Copy this security code in the Change Account Plan form, change the plan according to your new needs, read and agree to the prorated charge and then click the 'Change Plan' button to change your subscription plan.

# How can I change the billing information (Credit Card) for my eDoc Organizer Cloud Service Account?

If your credit card expires or you cancel it, be sure to update your account billing information by logging into the eDoc Organizer Cloud to avoid disruption of service. 

After you log into your eDoc Organizer Cloud service account at [https://cloud.edocorganizer.com/](https://cloud.edocorganizer.com/) follow the steps below to modify your subscription plan.

1. Go to Account > Settings menu and click the 'Change billing info' link under the Billing Information section.

2. On the Change Payment Method page, fill in the information of your new credit card and click the 'Update Credit Card' button.

_If your account is past due, your new credit card will be billed automatically for the past due charges and your account will be automatically activated._

# How do I Cancel eDoc Organizer Cloud Service Account?

After you log into your eDoc Organizer cloud service account at [https://cloud.edocorganizer.com/ ](https://cloud.edocorganizer.com/)follow the steps below to cancel your account.

1. Go to Account > Settings menu and click the 'Cancel Account' button.

2. Fill out the requested information and click the 'Continue Cancellation Process' button.

3. You will receive an email with a link to cancel the account. Click the link to complete the cancellation process. Please check your Spam folder if you don't receive an email after completing the step above.

4. Click the 'Permanently Cancel Account' button to cancel your eDoc Organizer cloud service account.

5. You will receive a final confirmation email stating that your account is closed. 

# How can I migrate my eDoc Organizer Home Edition data to the Cloud Edition?

1. Sign up for an eDoc Organizer Cloud Edition account at [https://cloud.edocorganizer.com/ ](https://cloud.edocorganizer.com/).

2. Create a local backup of your eDoc Organizer Home Edition data using the File > Backup menu item in eDoc Organizer Home Edition.

_Note: To ensure successful transfer please ensure that you have signed up for the appropriate plan with enough storage space in eDoc Organizer cloud edition to accommodate all your data. If you are not sure, we recommend that you signup for a plan with higher storage allocation and then reduce it once your data has been transferred successfully. You can get a rough estimate of how many documents you have and what their sizes are by opening eDoc Organizer Home Edition and pressing Ctrl+Alt+O key combination in the main window. This will open the location on your computer where all the documents are stored. Right click on the 'Document store' folder and click on Properties to see how many files and the total size of that folder._

3. Download and install the Cloud Migration Utility from the following link: [http://www.edocorganizer.com/Downloads/CloudMigrationSetup.exe](http://www.edocorganizer.com/Downloads/CloudMigrationSetup.exe). The Cloud Migration Utility can take a eDoc Organizer home edition backup and migrate it to the cloud service.

4. Run the Cloud Migration Utility. Enter the credentials of the eDoc Organizer Cloud service account and point the utility to the latest backup from your eDoc Organizer home edition. Click the 'Start Migration' button to start the upload of your data to the cloud account. 

_Note: Depending upon your internet connection upload speed it might take a few hours to upload your documents. The upload should not be interrupted as you might end up with duplicate data if you run the utility more than once.  If there is an error during the upload, it is recommended that you delete the data in your cloud account before re-running the utility._

# eDoc Organizer Advanced Search Syntax

eDoc Organizer search query is broken up into terms and operators.

**Terms**

There are two types of terms: Single Terms and Phrases.

A Single Term is a single word such as "_Invoice_" or "_Bank_".

A Phrase is a group of words surrounded by double quotes such as "Bank Statement".

Multiple terms can be combined together with Boolean operators to form a more complex query (see below).

**Fields**

You can search for documents by their content, name, eDoc ID, label, label group or their comments.

You can search any field by typing the field name followed by a colon ":" and then the term you are looking for. Here are a few examples:

| Looking for |	Search term |
| Word ‘bank’ in the document |	_content:bank_ |
| Word ‘invoice’ in the title of a document | _name:invoice_ |
| Word ‘contoso’ in the comments of a document | _comment:contoso_ |
| Label ‘statement’ on a document |	_label:statement_ |
| Label group ‘bills’ on a document | _labelgroup:bills_ |
| eDocID of 123456 | _edocid:123456_ |

**Wildcard Searches**

eDoc Organizer supports single and multiple character wildcard searches within single terms (not within phrase queries).

To perform a single character wildcard search use the "?" symbol.

To perform a multiple character wildcard search use the "*" symbol.

The single character wildcard search looks for terms that match that with the single character replaced. For example, to search for "text" or "test" you can use the search:

te?t

Multiple character wildcard searches looks for 0 or more characters. For example, to search for test, tests or tester, you can use the search:

test*

You can also use the wildcard searches in the middle of a term.

te*t

_Note: You cannot use a * or ? symbol as the first character of a search._

**Operators**

**Boolean Operators**
Boolean operators allow terms to be combined through logic operators. eDoc Organizer supports AND, OR, and NOT as Boolean operators

_Note: Boolean operators must be ALL CAPS_

**OR**

The OR operator is the default conjunction operator. This means that if there is no Boolean operator between two terms, the OR operator is used. The OR operator links two terms and finds a matching document if either of the terms exist in a document.

To search for documents that contain either "Bank Statement" or just "Statement" use the query:

"Bank Statement" Statement

or

" Bank Statement " OR Statement

**AND**

The AND operator matches documents where both terms exist anywhere in the text of a single document.

To search for documents that contain "Bank Statement" and "Bank of America" use the query:

" Bank Statement " AND "Bank of America"

**NOT**
The NOT operator excludes documents that contain the term after NOT.

To search for documents that contain "Bank Statement" but not "Bank of America" use the query:

"Bank Statement" NOT "Bank of America"

_Note: The NOT operator cannot be used with just one term. _

For example, the following search will return no results: NOT "Bank of America"

**Grouping**
eDoc Organizer supports using parentheses to group clauses to form sub queries. This can be very useful if you want to control the Boolean logic for a query.

To search for either "123456" or "896574" and "invoice" use the query:

(123456 OR 896574) AND invoice

This eliminates any confusion and makes sure you that invoice must exist and either term 123456 or 896574 may exist.