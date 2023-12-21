## 01/11/23
- Missed standup
- Contact Daniel Beavis
- Biscuit rota pr updated to include Andrew hough
- Ali contacted me w/ nav service
## 02/11/23
- Missed standup
- Pulling package successfully after contact Daniel beeves
    - Needed to specify the exact repository to pull from instead of pointing towards the THG-IET space
    - Pushed changes and the security/snyk check is failing
    - Contacted engagement about this problem - I don’t have a snyk account and can’t check the error.
- Helping David from engagement with Apollo write access
    - Can’t pull a package from Github’s engagement space with 401 error. Investigate what account Apollo is using to pull this
    - He found out that the workflow doesn’t parse in his PAT 
- Nav service team contacted me and endpoint returning 200 OK now, but sitebuilder config still return false for nav service config
## 03/11/23
- Chase engagement for snyk license help
    - Responded w/ a screenshot in the late afternoon, two security issues introduced
- Call Ali on Apollo GitHub package access work.
    - Made change, tested via opening a PR set to merge into David’s branch
    - Let him know
- Updated bigdaveclientinterface README to include new installation instructions as its a github package rather than an artifactory package now.
## 06/11/23
- SLS
    - Snyk security check passed, asked three reviewers (Catalin, David and Jon Clarke) to resolve their conversations if they’re satisfied.
    - Jon Clarke still wants activemq and camel to be replaced by themis-activemq package. Also wants the packages to connect to the backend instead of the front end.
- Reviewed Simone’s site manager UI PR about refreshing values
- Clarified to David from Engagement why the test check for my PR into his working Apollo branch is failing
    - Test check failing at the dependencyCheckAnalyze task, which he has commented out on his branch.
## 07/11/23
- SLS
    - Attempting to replace AMQ & Camel with themis-AMQ, using cart service as documentation
- Sd ticket on adding engagement org to okta for sa big Dave account has been done and closed
- Retro
## 08/11/23
- SLS
- Sprint planning
## 09/11/2
- SLS
## 13/11/23
- Miss stand up
- Redirects - support and debug the input files
    - Wolsey
- Firefighting
    - Raregames configuring live kraken returns error. Contacted Diogo matos, an engineer for kraken to ask for recent error logs pertaining to raregames
    - Released big Dave
    - Error still ongoing, talk to mars service engineer siva
## 14/11/23
- AL
## 15/11/23
- Firefighting
- SLS
    - Many things are breaking: themis-amq replacing basically 6 packages in total that are related to amp and camel
    - Getting it to a state where it builds
## 16/11/23
- SLS
    - Back-engineer themis-amq
## 17/11/23
- rug doctor, Tesco
- SLS
    - Call Ali/Ihor
- Firefighting
## 18/11/23
- SLS
    - Call Ali
## 20/11/23
- SLS
    - Contacted David from engagement if he knew more about the Themis amq package
- Pick up some reviews
21/11/23
- Retro
- SLS
- 1-2-1 w/ Andy
## 22/11/23
- SLS
    - No contact from catalin
- Reviewed some PRs
- Sprint planning
## 23/11/23
- SLS
    - Contact Catalin to ask for when they’re free
## 24/11/23
- SLS
    - Chase Catalin
## 25/11/23
- Fernanda Wolsey and Homebase redirect failing on TP with vague error message
- Chased Catalin, no response
## 26/11/23
- Catalin 
## 27/11/23
- Properties UI kick off meeting
- Catalan
    - SLS
- Looked at remaining tickets
## 28/11/23
- Release big Dave
    - Image task failing: fixed
    - Released on PL but health check returns ILL
        - Missing DB change
- 1-2-1 w/ Andy
- Did 2 training modules
## 29/11/23
- Rest of Training modules
- Hourglass
- Release big Dave
- SLS
    - Call with David and Catalin, had to update themis-amq to send headers as well
    - Their release pipeline having trouble so they waiting for Daniel beavis response
- Tech townhill
## 30/11/23
- SLS
    - New version installed. Having trouble getting docker to run on it again - asking for permissions that it didn’t before when I ran the run task
- Chased SD ticket on adding engagement GitHub okta to sa account
    - Rana got in contact