## 01/02/24
- Sprint planning
- SLS
    - Release change in BD removing endpoint first, then remove corresponding endpoint on SLS and then release and test on PL
    - David off Wednesday next week for 1 week until first day of week after.
## 02/02/24
- BD POST endpoint /subsite/{uploadId}/{environment}/service-configuration/configure -> Social login service.configure()
    - Check if configured
        - No: 
            - then PUT to SLS/api/v1/setup/redirect/domain/:siteId. 
            - Which in SLS calls addRedirectDomain in siteController
                - Gets siteName via siteService. Need to keep redirectUrlService’s isValidRedirectDomain + addValid RedirectDomain
        - Yes: nothing happens
- Sitebuilder setup social login which calls BD PUT /api/bigdave/social-login/create-site/${id}
    - Which calls SLS /api/v1/setup/site/:site and calls siteService.addNewSite()
        - What my BD event driven changes replace so far
## 05/02/24
- Test and debug new changes to SLS
    - Inconsistent startDocker task
    - Finished and asked for review
- Call with Ali 
## 06/02/24
- SLS
    - After multiple calls and testing it’s ready for release
- 1-2-1 w/ Andy
    - Sam Haines update feed manager certs expired jan 25
## 07/02/24
- Navigation service
    - Most recent version’s nav service 
## 08/02/24
- Call in the afternoon to release SLS
    - Moved to hopefully Monday
- Nav service release
    - Release tomorrow 
- Picked up ticket to update GitHub actions for Apollo do display correct health checks
## 09/02/24
- Chase up on when to release nav service
    - Evgeny wants to release a separate version first, which hasn’t been done today
- Continue with ticket to update apollo GitHub actions in meantime
## 12/02/24
- SLS release
    - No response from David
- Nav service release
    - Done
- Andy
- Firefighting 
    - 6 redirect tickets -> 4 now
## 13/02/24
- Apollo ticket
- Retro
- 1-2-1 w/ Andy
## 14/02/24
- Sprint planning : moved to tomorrow
    - Add ticket: remove event driven replaced relevant nav service bits from big Dave
    - Add ticket: monitor the release of SLS 
- Apollo health check solution
    - Waiting until Simone’s Apollo release is done.
## 15/02/2024
- Sprint planning
- Pre-release newer Apollo health check solution
    - Finished
- Picked up Navigation service duplicity removal from bigdave
- Finished training link from THG people
## 16/02/2024
- Carry on with Navigation service duplicity removal from bigdave
    - Noticed issue with setup being around site instead of subset and arrange for a rollback on Monday
## 19/02/2024
- Refactor nav service
    - Revert has been done
## 20/02/2024
- Chase engagement team for an update on when to release SLS
    - Released to pl and uat, gb1 & gb4
## 21/02/2024
- Navigation service ready the PR
    - Ask for a review
## 22/02/2024
- Chase on review
- Carried on removing duplicity from scratch
## 23/02/2024
- Chase on review
    - Evgeny wanted. Another team member to review it, and that review was pushed back to Monday as it wasn’t urgent
## 26/02/2024
- Chase for review and release
- Change DC password
- Joined knowledge share
## 27/02/2024
- Chased nav service, Emmanuel said can’t do review today as he’s swamped
- Tried to get big Dave running on vscode, nothing
## 28/02/2024
- Retro
- Sprint planning
- Pick up decommissioning site importer VM ticket
    - Deleted zabbix alerts for site importer
- chase nav service pr review
## 29/02/2024
- Chase nav service
    - Has reviewed, asked for several strings to be added to the env files and pulled in that way
- Continue decommissioning site importer VM
    - Shut down VMS
    - Created sdp ticket on deleting dns records and load balancers and pinged on networks channel
- Engagement David asked for where to go to change site config