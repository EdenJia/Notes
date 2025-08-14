## 01/07/2025
- Chase linux team
- Brush up on Apollo and start preparing for future knowledge share
- Self review
- More trees tech monthly report generation
- James mercer asking about fulfilment
    - Also saying confluence admin passed to another security team and trying to talk to them
- Double checking db connection url updates for live Elysium release. 
    - Releasium changed but not released. Need to figure it out by tmrw
## 03/07/2025
- Live Elysium db migration midnight
    - Apollo, bigdave, propservice, site importer, releasium
    - Follow up today on debrief and filling out documentation on app statuses, recognised issues
- Properties service load balancer endpoint
    - Infrastructure api has get endpoint to check load balancer
        - I do not have eligible roles to use the api
        - Asked William
    - Site content ui connects to gb1
    - Lbv, no load balancing, encryption, protocol ssl_bridge, certs on servers instead, no content switching
    - When traffic comes in, it sent to all same environment server , which k8 managers where it sends traffic to pods
- Moretrees tech: Adam lowe main stakeholder leaving next Tuesday and introducing two new people. Matt Devitt for sales and Hannah tear for commercial (monthly finance reporting). 
## 04/07/2025
- Resolve some more tree victops issues
- Fulfilment frank issue: resolved
    - Jack watt a delivery manager (DM) franked with wrong detail
    - Found out cannot log in to sdm app via Okta 
    - Made sd ticket
    - Contact Andrew hough for a meeting to take advantage of his access
    - Big Dave process:
        * "{call ™”
        *       + "(:Name, :BE_SiteCode"
        *       + ", :Channel, :Packaging_Group, :Skip_Checks )}";
        - Call sproc in dbmanager tabernus
        - The sproc change for site code: 
            - Order_Manager.dbo.Channel : channel
            * Catalogue.dbo.Site: Site, Store_Name
            * ChannelManager.dbo.channel: channel
        - Creates fulfilment created event and send off
- Sent mail about releasium decommission
    - Ian han has contacted me about what to do instead
    - Jon Clarke wants a meeting to discuss
- Elysium db migration plan standup
- Self review
    - Big up company impact
    - Big Dave, sitebuilder, site importer api, site importer ui, redirect configurator, redirect engine, properties service, releasium, Apollo, more trees (project service, transaction service, user management service, ui to name the main 4), client portal
- Next week: overview of site automation applications and common debugging steps
- Moretrees dlq
    - Invoice expired messages
    - Manually moving from dlq until sdm access restored
## 07/07/2025
- Resolve moretrees dlq 
    - 3 invoice expired jobs 
- Create general knowledge share of site automation applications for on call / firefighting issues
- Big Dave using external diamonds metrics. It is soon being decommissioned end of year. Need to migrate to alternative service e.g. grafana
## 08/07/2025
- Ask for feedback
- Personal development TDD
- Failover from gb4 -> gb1 cancelled on the 10th
    - Failover at 31st July if all goes well
## 09/07/2025
- GitHub PAT expiring. Replacing namespace secret dockerconfigjson and site builds runner secret with lifetime PAT
- Elysium smoke test plan standup
    - Confirm whether smoke test tonight or not
        - Going on Friday morning
        - I’m on AL Friday so need to sort that out with Matt.
    - Concern about disabling logins
        - What do I do. Switched to the aao url but still disabled get 503 errors.
    - Will be 2 others next week.
        - 16/07 Wednesday morning
        - 18/07 Friday morning
    - More in future
        - 22/07 Tuesday morning
        - 24/07 Thursday morning
    - Full test. Date to be confirmed
- General knowledge share
    - Ask for feedback from William and cash
        - William wants more details on the redirects
- Knowledge share site automation
    - Another one of how to monitor for smoke test
    - Talk initially about the smoke test planned. And on Friday which I won’t be in for.
        - It will be Tash
    - How to monitor site automation apps and what to expect.
- New confluence page by matt about on call processes and incidents 
## 10/07/2025
- Talk with tash, josh and will on smoke test rota for next 2 weeks
- Talk with tash about site auto’s smoke test
- Getting bunch of permissions on tp people’s accounts
    - AD and DC roles given. Kyle says anything else is gotten somewhere else
    - Find tools.io.thehut.local permissions. They’re not included
    * SCU-user, requested and sent to staff tech
- Db decommissioning
    - Check up on ares db status: still in progress
    - Start site info api db decom
    - Thg status namespace in gb1 gb4 not terminating because of finaliser needs deleting. K8 support helped
        - Submitted db decomm ticket.
- Redirect manager on TP issue
    - Ask to submit ticket on redirects board
    - Ryan nixon ABFD with error
## 11/07/2025
## AL
## 14/07/2025
- Tp team still does not have access to site content UI
    - Put in another role access req - josh able to access site content ui now
- Continue decommissioning 
- Find out about this week’s smoke tests
    - Move live relevant apps to gb4 for smoke test tmrw
        - Sitebuilder on gb1, failover to gb4 done
        - Moretrees already on gb4
- Sitebuilder issue with look fantastic subsite frank
    - Ingenuity check failing. Need to create New_Site_Created record for it.
    - Other lf subsites were franked before this check was in place
    - Insert data manually
## 15/07/2025
- Create bash script for pulling artifactory packages and uploading them to THG-IET
- 1-2-1 matt
    - Joining sprint planning
    - Shell console
        - Migration/ Refactor java backend with William
- Knowledge share
    - General knowledge share
    - Moretree knowledge share
    - Redirect process knowledge share
## 16/07/2025
- Ameliorate fr and it decomm redirects not working
    - Missing dns / cname addition from networks team
- Update that documentation of decommission halted
    - Give tick or not column
- Bash script is not viable. Some packages do not exist in artifactory frog ui
    - Individual investigation is needed
    - Creating an isolated blank spring boot application just to test individual package downloads
- Added to group chat about stock owner missing thehut id 0
    - Fds api does not have id 0, 
    - Supply chain ownership service team says fds api is the source of truth
    - Pushed a hacky solution to stick thehut on the sitebuilder UI
    - Where I was added. Told them sitebuilder ui and api was in maintenance mode and not currently able to be developed on, redirected to matt Gregory, my manager, to coordinate tasks.
## 17/07/2025
- Continue big Dave maintenance
    - Thg-gradle-plugin’s most recent version removes artifactory dependencies but isn’t released as a package because of pipeline issues. Engagement team looking into it.
- Stock owner group chat
    - Matt Gregory added and shared history
    - Matt pushed back, saying the change should be on fds side because their api is the source of truth
- Elysium smoke test planning
## 18/07/2025
- Elysium smoke test 4
- Big Dave maintenance
    - Keep an eye on engagement chat
    - Continue implementing other artifactory migrated packages
- Alix contact about developing product restriction bulk upload feature on site content ui
- Jack watt contact about submitting wrong field in a fulfilment site setup on sitebuilder
## 21/07/2025
- Jack watt prioritisation on fulfilment site fix
- Richard gill contact about business-units failing to create look fantastic for thehut
    - Sage automatically bans business unit creations on stock owners of id 0 - which is thehut
    - Followed up in shared group chat with details and working on resolution. Ezra says B0001 already exists for selection as a business unit
- E2e testing evolution with Tashfeen and TP squad
- Bigdave login fail for ST or PL 
    - Ian p didn’t migrate st and pl db connections to aao elysium
    - Prioritise big Dave maintenance tmrw
## 22/07/2025
- Prioritise big Dave maintenance now
    - Building successfully,
    - Refactored code to use new import paths and class names from dependencies
    - Tests all pass successfully
- Elysium smoke test
    - Prop service CRIT health check. Going down. Work with SRE k8 to figure out what is going on.
    - Prop service no caching
- Jack watt contact about trouble setting up fulfilment site sixsto. Error message on sitebuilder says catalogue code already exists, therefore fulfilment site is already set up. Have a more meaningful error message in the future
## 23/07/2025
- Big Dave maintenance
    - Sd ticket to get permissions for big Dave service account
        - Thg-dataandai
        - Thg-applicationsecurity
        - Thg-product
        - Thehutgroup
    - Rework workflow tasks to include authentication to GitHub, if it isn’t there already
    - Push existing changes to GitHub to set a benchmark failure for the build and test task that runs automatically
- Elysium smoke test planning
    - George Dooley team set circuit breaker for properties service
        - Look into how to set circuit breakers automatically instead of manually
## 24/07/2025
- Big Dave maintenance
    - Chase windows team on service account roles
    - Asked for review from another former teammate, java guy in a  team
    - Test releases all day to resolve deployment errors
    - Done and released
- Started properties service maintenance
- Elysium smoke test 6
- hourglass
## AL
## 29/07/2025
- Fix Apollo deployment pipeline issues -> park ps maintenance as it’s probably same issues.
- Tash:
    - Write ticket on apollo side for what Jon asked 
- Big Dave :
    - Event serialisation failed for product
        - Javax bigdave, import Jakarta from representation jar
            - Revert helm to previous working version
                - Helm list
                - Helm history <helm list name/k8s-gb4-live> -n <namespace/bigdave-api>
                - Helm rollback <helm list name> <revision number> -n <namespace>
    - Future solution: Java version upgrade to 11 -> 17
- Apollo
    - Search team wants to increase limit
    - Deployment pipeline stuck
        - the pl deploy job was using gb5 runners - changed to gb4 runners
        * Reverted William’s changes
* Fulfilment clubl product manager
    * Missing values tables in catalogue db
        * Pricing_band
    * All other values are created
## 30/07/2025
- Fill in hourglass
- Support apollo release and testing
- Big Dave meeting afternoon
    - Event from representation from engagement
        - short: move event class from representation jar
    - Find out the archived process subsites
    - Find representation system for user process for site franking, and site decommission
## 31/07/2025
- Investigate more trees tech dlqs
    - Transaction.payment.job.expired-3ds: 4173129
        - Account ledger id ^ unattached to an existing account ledger recipients entry. Set account ledger entry to status 0 inactive. Observing for later.
    - App runtime gh action changes on all workflows. Due of august
- Big Dave representation event transfer
    - Reviewed and releasing
- Ecomm decomm
    - Contacted Marc Hamilton to figure out how the subsites are archived
        - Site manager has a tick box to make subsite archived
        - A separate tick box to say subsite is live or not
    - Contacted Jon Clarke and a list of subsites to be decommed, whether they’re live and archived is sent to me
- Big Dave handshake with tash
    - Deal with firefighting 
    - Move the 20 pointer into separate tickets into the TP squad backlog
        - 2 weeks worth only
    - Created site automation project, check thg flow tmrw