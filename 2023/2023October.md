## 02/10/23
- Chase redirects
    - Equine premium redirects
- SLS
- Reviewed Simone’s ticket on redirect manager error refactor
## 03/10/23
- SLS
    - Got an error that refuses multiple consumers: Failed to start route route3 because of Multiple consumers for the same endpoint is not allowed: direct://serviceConfigured
- Redirects
    - Equine premium redirects are done
## 04/10/23
- SLS
    - Call with Andy then later Ihor : asked for more details from David from engagement who made the comment asking for refactoring to avoid java reflection
- Cameron noble asked for ABFD redirects
## 05/10/23
- SLS                                 
## 09/10/23
- SLS
- Review Apollo ticket but Ihor beat me to leaving the approval
## 10/10/23
## 12/10/23
- SLS: David came back - Instead of releasing on PL, run SLS locally but connect to the PL queues and test via sending event to PL BD.
    - finished testing via local SLS connected to PL services and my changes work smoothly
    - What’s next? Since PL testing is already ok
- Picked up the Wolsey redirects ticket
    - More than half of the source urls didn’t have a starting forward slash
## 13/10/23
- Shadow Ali on setting up UAT
- Setup Beaver
## 16/10/23
- Created 6 DNS request SD tickets for ABFD networks’ domain, checkout, horizon-api
- DB data insert for all beauty
    - Main data: 366, Site_Code=allbeauty, Locale en_GB, Subsite_Code: en, domain: https://allbeautyen.ingenuityuat.net, checkout: checkout-allbeautyen.ingenuityuat.net, horizon: horizon-api.allbeautyen.ingenuityuat.net, 
- Service configuration with Ali & Simone on UAT service configuration for AB
    - Didn’t finish SLS setup
- Firefighting: reverting authorised stage of protexin
- The x planet earth training module
## 17/10/23
- AB UAT: missing TP service config setup
- Fd uat
- Firefighting:
    - missing ability to add business units via sitebuilder for subsites
    - ticket to show legal entity and business unit from sage in backlog given to Simone but missing bits: legal entity and business unit components not populated in UI
    - When setting up sites, the search bar + dropdown component does not populate with a set value (if already selected previously) as placeholder
    - Protexin not setting up nav service correctly, there were two subsites en and us with the same domain and rich had to manually update the domains to fix
- 1-2-1 w/ Andy
    - Clean out old records: set up protexin and it’s fecked
        - Remove 381-en 
    - Grad title
## 18/10/23
- Nav service
- Your Coca Cola redirect
## 19/10/23
- SLS
    - Uncommenting event consumer code and its tests and fixing check style failures because of these
- Backfilling of data needed for big dave now that sage is running as expected again
## 20/10/23
- Redirect ticket
- SLS0
- Nav service investigation
## 23/10/23
- Call with Ali on adding patset certificates
- Chase up nav service up
- Contacted engagement for SLS snyk tasks failing
- Call with Ian about the active redirect tickets
## 24/10/23
- Chase nav service
- SLS PR
    - Merged master’s changes in, had new pull request check tasks and project now building anymore
## 25/10/23
- Chasing nav service 
- SLS
    - Packages in there moved to GitHub from artifactory so don’t look in artifactory anymore in build file
    - Suggested to move the two outlier packages to GitHub
    - Redirected to Daniel beavis, a senior
    - He said the build grade detects packages released through GitHub, bigdaveclientinterface has never been released through GitHub and that’s why it’s not being detected
    - He has created a PR to add release workflow for bgci that me and Ali can’t review properly so I asked Craig if could take a gander
## 26/10/23
- Security update I’ve been deferring for -34 days now?
- Chase nav service
- SLS
    - Moved to block
- A few call with Ian where he updated me on his investigation into redirects 
- Quick call with Ali
## 27/10/23
- Hourglass
- Got bd client interface done
    - Contacted Daniel beavis to release
- Pick up and review tickets on the BGD board
## 30/10/23
- Release big Dave client interface
- Pick up some reviews
## 31/10/23
- Bd cli released on GitHub, still have the same error where the package isn’t recognised
    - Contact Daniel Beeves
    - Called Ali for help - the PR removed artifactory related files/code.
- Hourglass