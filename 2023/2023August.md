## 03/08/23
- SLS
    - Local Big Dave doesn’t receive the serviceConfiguredEvent
    - Check on ActiveMQ PL queue shows 2 consumers, my local BD and the PL BD listening on the serviceConfigured queue
## 04/08/23
- Sending serviceConfigured event but not receiving it on Big Dave’s side
    - Googling says it’s caused by AMQ fail over. The connection object is not getting started at consumer side in such cases
## 07/08/23
- Firefighting: 
    - Biokult blog redirects: redirected to DL-Blogs
- SLS
    - Testing on activeMQ PL’s queue with two consumers only has the first consumer consume the message, which is the PL BD, so those messages would never reach my local build
    - Asked tech engagement to get locally run SLS connect to the activeMQ local image
        - Done so
## 08/08/23
- Firefighting
- SLS
    - org.springframework.dao.DataIntegrityViolationException: PreparedStatementCallback; SQL [INSERT INTO bigdave.dbo.Service_Event_Log (Site_Id, Subsite_Code, Service_Name, Time_Stamp) VALUES (?, ?, ?, CURRENT_TIMESTAMP) ]; String or binary data would be truncated.; nested exception is com.microsoft.sqlserver.jdbc.SQLServerException: String or binary data would be truncated.
    - serviceConfiguredEventJSON: {"siteId":140,"subsiteCode":"site-level","serviceName":"SocialLoginService"}
        - Error caused by subsite code value being higher than 2 chars
    - Adding the activemq config properties to pl and live files, confusion between config/ and k8s/ folder
## 09/08/23
- Sort out the config, put into review and bother engagement for a review
    - Working on pull request and adding unit tests
## 10/08/23
- Continue with unit testing and writing the PR
- Firefighting:
    - Biokult UK redirects
        - [RDIR-18] Speech marks
        - Blog redirects [RDIR-17]
            - Blog team says we have to do it since the pages redirecting to the blog are missing the blog custom slug
            - Asks her to try re-uploading since we have new changes on TP to allow trailing slashes
    - Toblerone UK redirects
        - Speech marks
        - Feature the faq list question headings in speech marks, then add comma and a /faq.list as source, then as target: https://www.toblerone.co.uk
        - Asked reporter to attach original spreadsheet
- 1-2-1 w/ Ali
    - Helped me fix a broken test
## 11/08/23
- Fixing PR failed tasks, review PR
    - Fighting check style errors: illegal import for java.util.date and org.joda.time.DateTime
    - Illegal catch exceptions: even though exception is thrown by camelContext
- Firefighting / redirects
    - Toblerone UK 404 redirects
    - Biokult UK
        - RDIR-18 Yuilya came back with leftover redirects that aren’t inserted into TP. They had speech marks and typos e.g. .pdff in so asked her to fix those and try again in TP
        - RDIR-17: responded to that ticket. asked if she needed to ‘delete all redirects first and upload again’. Said to do so to existing redirects that had the same source urls for biokult
## 14/08/23
- Fix the last failed tasks
    - Finding alternatives for Date and DateTime
- 1-2-1 w/ Andy: Off boarding process at end of month
## 15/08/23
- Continue w/ SLS
    - Deadlock in illegal exception handling
        - addRoutes() from package camelContext throws Exception
    - Deadlock in illegal import: joda.DateTime
        - joda.DateTime required to set the event field happenedAt from the package ‘representation’
    - Fixed illegal import util.Date needed to set the happenedAt event header by removing the setHappenedAt() method
- Retro
## 16/08/23
- Sprint planning
- SLS
    - CheckstyleMain suppress warnings done
    - Spotbugs
    - Check now failing at autolintgradle where it could not download a spring dependency
        - Written message draft to engagement, to be sent tomorrow
- Redirect
    - Investigating broken redirects in Toblerone asked Beatrice to check the source urls
    - Duplicate redirects for biokult blog redirects
## 17/08/23
- Ask tech engagement for help
    - Artifactory issue
- Redirects
    - biokult: 
        - blogs: duplicates because Yuliya couldn’t bulk delete 495 (got error). Asked her to send me a file of these duplicates so I can bulk delete them for her.
        - Additional ones inserted 
    - Toblerone: no response yet 
- Call w/ Azky & Ali
## 18/08/23
- Chase up engagement for a review
- Call with Ali to help with demo prep
- Redirects 
    - Biokult redirects: I’ve bulk deleted what Yuliya wanted, she tried to upload via TP but got error. I’ve investigated and her inserts are there in the DB aside from 1.
## 19/08/23
- Engagement for PR review
    - 3 people reviewed it 
    - Fixing requests
- Redirects
    - Biokult
        - Call with Ali to find missing 
        - Yuliya says automatically removing trailing slash after pulling redirect through even though it is saved with trailing slash in Elysium
        - Cache problem
- 1-2-1 w/ Andy
- Change the biscuit rota
    - Remove Craig and Ian, add Ihor
## 20/08/23
- SLS PR
    - Make a separate class for camelroutebuilder that includes an error handler
- Redirects
    - Investigating a redirect chain when it isn’t in Elysium DB
## 21/08/23
- SLS
    - CamelRouteBuilder class
        - Not sure need to incorporate all these new classes
- Contacted DL-Blogs, they say the /health-hub to /health-hub/ 
- Working with Ali on his sage testing
## 25/08/23
- SLS
- Retro
- 1-2-1 w/ Ali
## 26/08/23
- Sls
- Redirects
- Sprint planning
## 31/08/23
- Hourglass 
- Networks team Chris foley called to ask for me to test new changes on redirects side.
    - 31.177 find gb1 ip and then curl
        - Manipulate dns /dns lookup