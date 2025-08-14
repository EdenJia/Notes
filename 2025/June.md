## 02/06/2025
- Hourglass x
- Complete mt backlog tasks
    - Check mt amq dlq x
    - Account deletion x
    - Monthly report generation x
    - Account investigation x
- WFH req for friday approved auto
## 03/06/2025
- Auth0 suspicious behaviour
    - No email, just ip address down to a ISP in Mumbai India
- Prep PRs for ticket to change runners back to gb5
    - Bigdave failed to build with thg-gradle-plugin missing
    - That grade has migrated to GHCR. Attempting to migrate bigdave build file to use new GHCR.
        - Running into build issues
        - Asked engagement for help
## 04/06/2025
- Mt platform service dev status is up yesterday in pingdom alerts channel
- Main focus: Kevin Jackson doing prop service. Make it java 11 -> java 17
    - Spot bugs main and test errors
- Releasium adding a notice to say decomm soon
- Thg-gradle-plugin audit as it’s decommed from artifactory.
    - Big Dave pr
    - Site importer api pr
    - Redirect configurator merged in
    - Apollo merged in
- Decom
    - Archive repo
    - Get DB details if using, host, user, db name, 
        - Raise sd ticket to get dba to decomm 
- Moretrees reqs
    - Amq dlq 
    - 3 account deletions
    - 1 account missing roles
## 05/06/2025
- Java migration for properties service / manager
    - Resolved spot bugs and check style warnings and errors
    - Got application to run on docker
    - Pushed to PR. currently WIP
## 06/06/2025
- Review and plan to release
## 09/06/2025
- Protexin pet uk wants to change domain from www.protexinpet.co.uk to www.protexin.com
    - Trace thru bigdave. 2 tables, nscu and ingenuity test servers. Actioned
- Redirect request bulk delete came in. Asked for them to come in a CSV
    - Need a trickle script. Waiting for tickets to come in. Got scripts set up
- Review and Release properties service
- Moretrees dlq
## 10/06/2025
- Moretrees dlq investigation
- Check out amq st announcement prop service 001 doesn’t work, change to 002
## 11/06/2025
- Prop services pipeline fix amq
## 12/06/2024
- AMQ DLQ investigate 4 invoices
    - Ids: 4161124, 4161154, 4161157, 4161158 all modified 2025-04-18
    - Ids match account_ledger table ids, all are most recently modified by 3623063, a user that has been deleted 2025-04-25, created 2025-04-18
    - All invoice ids have the same account id 3623064 as well
    - mt-transaction-job contains logic on how the message is sent
        - Calls on account ledge entries that are, status = 0 (inactive), created less than 30 days ago, and are of type bank transfer. These four account ledger entries are found
        - Send those messages off
    - Mt-transaction-management-service receives those messages and logs the invoice Id out.
    - If mt-transaction-job fails, it catches the exception but just logs out the invoiceId, not the exception details so we don’t know why.
    - Elastic search/kibana does have logs from other services receiving the expired bank transfer invoice event  sucessfully -> com.thg.transactionmanagement.messaging.consumer.InvoiceConsumer - so some invoice expired events. These 4 events are just specially failed. 
    - Move those messages on and then wait for the next set of failed dlqs and compare invoice ids. If same, then this account ledgers’ deleted user is why
- Added to Infrastructure maintenance 
## 13/06/2025
- AL
## 16/06/2024
- Thg training
    - Ai module, new phishing module, imposter syndrome
- Continue investigating new amq dlq messages for more trees
    - Need to check logs in appruntime
    - Need to gain access to argocd, asked k8 support, then make rg/sg access req on sdp
    - So message is being received in mt transaction management service but not found exception happening at message consuming stage, does not have a error handler so spring jms thus redeliver the message and eventually dump in dlq
    - Method failure: mt-transaction-management-service/service/impl/MailServiceImpl.java sendMailInvoiceExpired()
        - purchaserFullName is empty. Checked db but it does have matching user Ids with names
        - Replicate the method behaviour, but no way hos-say
- DL_BigDaveSupport add to email group make a sd ticket. Done
- Libs-release plugins-release not needed anymore, will just have to use maven.github.pkg equivalent into repos of build files
## 17/06/2025
- Send Ian the argocd roles needed for more trees
- Amq dlq more tree 
## 18/06/2025
- Amq dlq more trees
    - Payment.job.expired-3ds queue: 4168122
- Adhoc more trees user login and widget
    - Fixed
- Write up more tree process for creating new auth0 user and what to respond with when they have widget issues
- Don’t have write access so chasing the right people before trying to find a confluence admin
## 19/06/2025
- Investigate expired-3ds queue. It’s an incomplete transaction on stripe but set as requires_Action (2) status on corresponding account_ledger entry in DB.
    - Other incomplete payments on stripe are not in account_ledger table. Suspect those were deleted
        - Followed the code and If transaction type is TRA_BTC then set status to 5.
        - Did that instead of deleting the entry. Hopefully I didn’t f up
- Get write access to document some unwritten more tree BAU processes
- Getting authentication for artifactory because moving every package seem impossible
- Started migration big Dave artifactory pulled packages to equivalence in GitHub
## 20/06/2025
- Artifactory try authenticating using SA DC details
    - Works for connecting, but pulling individual packages get 401 still
- More trees checking on tanzania and Kenya planting
    - Kenya 300 from today
    - Tanzania 500 also asked what time. I’ll check tmrw
- More trees
    - Refund remaining credits on a customer’s account
- Getting more tree confluence write access
    - James mercer -> staff tech, staff tech -> space owner, Kieran dony -> Ian parkinson, Kieran done -> jack Owen
        - Give up and write supplementary documentation in the site automation space
## 23/06/2025
- Moretrees edit access from jack Owen
    - Jack doesn’t have access, referred me to tech admin, they do not have access to the confluence space so no leads there.
    - Write support doc in site auto space
- Chase artifactory chat w/ windows team
- 1-2-1 w/ matt
    - 3 objectives
        - 1. Support more trees
            - BAU tasks
            - Documentation
        - 2. Maintain site automation applications
            - Regenerating tokens, failovers, issue support
        - 3. Onboard onto ctp
            - Get roles, accesses, get some common applications running locally
            - Confluence space added to team, 
            - https://thehut.atlassian.net/wiki/spaces/TPUIDOCS/pages/4651810985/New+Starters+Core+Tooling+specific
        - 4. Onboarding site automation
    - Promotion - consistent objective superseding 
        - Matt gives 3 or more obj every half year. Mixture of things beneficial to business and personal career
        - H1 H2 performance review.
        - Skills matrix
        - If promoted in December, then could promo in July.
    - Current vision:
        - Doing more than expected.
        - Long term to join the team
        - See what site automation owns and what could be migrated and decommissioned.
    - Demonstrate capability in those services.
    - Longterm: Join TP team
    - 1-2-1 every fortnight with Matt -> then Tash will become manager
    - AL
        - Double time off notice
    - Start booking AL as meetings with Matt.
## 24/06/2025
- Run through console
- Check with Ian what we still own and what is decomm-ed already
    - Ares
        - DB not decomm-ed link for sd ticket in Ian’s documentation
        - Airlock dns still active apparently
    - Site importer api
        - Db in tabernus
        - Abbi head of seo, and ncleang are users June
    - Site importer ui
* Live
* https://tools.io.thehut.local/site-importer/#!/login
*  
* ST
* https://tools.st.io.thehut.local/site-importer/#!/login
    - Releasium
        - Need a release to let users know it is decommed, can it be still releases labelled 
    - Migration Elysium, what problems did you have with tuberous
    - Site info api 
        - Decommed excepted db
    - Status and api 
        - Decommed but DB still active
- Think about what career goal you’d like
## 24/06/2025
- Ask Ian about elydb migration
    - Asked him to copy and paste all his roles across Cerberus and ecrm auth on his leaver’s document
- Personal dev
## ## 25/06/2025
- Moretrees bau tasks
    - Search db for total trees planted on behalf of: GWRm. Rust greater wester limited, redrok (28800A)
    - 120DC3 previous tree planting numbers, the project and the date
- Linux team got back about artifactory auth issues
    - Paul de’ath fobbed me off to Kevin irvanipour and Alvaro mema. Says they’ve had this issue and resolved it
        - Too much to do, on hold until bigdave issue resolved
- Bigdave health check ill
    - Db connection locked for user bigdave. Contact dbas
    - Resolved with Ian p and Andrew h
## 30/06/2025
- Properties proposal
    - Share details with api endpoint that accepts single locale
    - Share documentation in properties proposal meeting chat.
- On call discussion
    - So tooling on call is 150 gbp per week. More trees since Handover not compensated, Andrew hough on rota all the time for ingenuity implementation
    - Set up knowledge sharing sessions for Apollo troubleshooting
        - Made an initial onboarding site automation chat with matt, tash, William and josh
        - Listed dis, Okta groups, GitHub orgs, roles
- Talk with matt on decommissioned services’ status & work out the workflow.
- Linux team about artifactory credentials
    - Talk to kev jackson about solution
- Self review
- 360 reviews