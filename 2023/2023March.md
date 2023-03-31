## 01/03/23
- The next step is to implement an endpoint for the createSorryServerRelease() method, test and to test the restartSorryServerPipeline endpoint.
    - The first method actually creates a new sorry server release on GitHub so I want to be careful about testing this.
    - James Healy
        - Where would the ‘tag’ from createRelease come from
        - Find the latest release tag
        - Wait for deployment to finish or cancel
    - Written endpoint to create a sorry server release, started on testing the create sorry server release method
- Catch up w/ Ali 
- L& D session about being a more engaging person
## 02/03/23
- Testing and the trigger release endpoint keeps giving me bad request 400 error, called Ali and he got the same endpoint working
- Actioned Homebase redirects that came through yesterday
- Started on whoiselijah en checkout build
## 03/03/23
- Working on the create sorry server release endpoint - can now set the newest release tag, working on how to create that release on GitHub actions.
- Catch up with Andy
## 06/03/23
- Quick Procurement policy training
- Big Dave Sorry server changes - having trouble, haven’t made much progress 
- Started on the whoiselijah checkout build - trouble with the chrome driver for Mac, Mac rejects running it as it’s downloaded from the internet
## 07/03/23
- Call with Andy to sort this trigger GitHub release endpoint out
- Who is Elijah has asked for an eta on the completion of checkout as they’re due to move into iUAT today. So I want to prioritise and complete this today
## 08/03/23
- Call with Ali - Can create a sorry server release successfully through Github’s rest api
- Built whoiselijah checkout, got it reviewed and it’s in the process of being released rn 
    - Let the whoiselijah team know when it’s released
## 09/03/23
- Test the endpoint to restart failed jobs for a subsite on big Dave
    - Finished and in review, creating release ticket
- Whoiselijah test website released checkout build, spent time testing those changes
## 10/03/23
- Help Simone with her release for big Dave 
    - Filled in my column in the skills audit spreadsheet
- Released sorry server changes for big Dave afterwards
- Reviewed Craig’s PR on refactoring site builder
- Started looking into Ian’s PR on site details UI payment CRUD functionality 
    - Have issues running modular TP
## 13/03/23
- Call with Ian, went over what to test in PR and approved it
- Ensure that pingdom checks are created correctly through BD
    - Going through the code that creates the pinion alerts, seem to have many failsafes
    - Contacted staff tech about getting access to pingdom
## 14/03/23
- Follow up on staff tech
- Matalan trickle script
    - Call Simone
- When the releasing the pipeline errored - need to update publish.yaml GitHub workflow file for releasing properties service with new docker changes
    - Asked help from Craig
- Volunteered to interview senior
- Retro 
- Adnan: Google fonts is the most used fonts, keep downloading and uploading it onto CDN (a lot of duplication)
    - Download entire google fonts database, upload it on CDN and use on big Dave - 218MB
    - Save some money even though everything is cached
    - Save time downloading, keep in one directory
    - Lewis Callam, James Trevor, Chris Walker liked the idea
## 15/03/23
- Follow up on staff tech
- Fix properties service’s publish pipeline, released PS
    - Made much longer by all the approval checks throughout the gates
- Call with Andy to go over the interview tomorrow
    - 30 mins per person
    - Culture fit interview
        - Introductions
        - Interview Qs
        - Wider questions, allows more information
    - Finish scorecard by tomorrow
- Sprint planning
- Pingdom creation confirmation on big Dave - tried different upload_IDs that move past the edge case validations. Stumbled upon one that returned an error 400 bad request. So scrutinising that request and cross checking with documentation
## 16/03/23
- staff discount policy training
- Interview regroup and then interview later in the afternoon
- Pingdom
    - Integrationids parameter value is invalid, the expected value type is an array of integers and big Dave also converts it into an array of integers when converting the json to string. Next step is to check if integrationids exist in pingdom
## 17/03/23
- Review and submit interview scorecard
- Pingdom
    - Invalid integration
    - Put. Method in to check integration IDS exist or not
- 1 to 1 with Andy
- Vm patching
    - gb5, gb1, gb4 002 done, gb4 001 needs more disk space 128MB
## 20/03/23
- First priority - Rollback to previous spacewalk snapshot as upgraded docker version incompatible with bigdave
- Sudo docker ps, sudo systemctl restart docker.service, Jenkins -> Themis-universal-bounce, build with params, bigdave, env=li-gb1 002, build, go into job, 
- Senior engineer Interview 
- Call with Ian to go over his changes on site details UI
- Reviewed Craig’s PR on sorry server url change and asked for a change
## 21/03/23
- Start firefighting two issues popped up yesterday
    - Franked subsites have subsite status NULL, could it be 0 instead
- Pingdom access ticket wasn’t even in the queue, it now is and is assigned a technician
- Investigated user activity logging on modular tp, turns out it was atomatically done via jaguar and stored on google cloud platform
    - Found the logging and it was listed as Modular Teepee, with nothing to distinguish it from a site details activity other than the username of the one who was logged
## 22/03/23
- Continue investigating site details logging
- Chase up on Pingdom access
- Picked up ticket to investigate how to allow traders to enable/disable wish lists on site details
    - Site manager has a few configs for wish lists, wasn’t sure if the Wishlist config we’re changing has separate effect on the other Wishlist configs
    - Called Ian on this, he directed me to Rich as that required knowledge on Elysium
    - Asked Rich on this and he confirms the all the configs can be enabled and don’t affect other configs
    - Added that detail to the spike ticket and put into review
## 23/03/23
- Moved SPIKE ticket on enabling wish lists for site details to done
- Asked to shadow Craig on the big Dave ICE ticket
- Gillette EN redirect from Sana Farooq
- Anti bribery & policy on gifts and hospitality training
## 24/03/23
- Helped Ali with running redirects manager
- Reviewed the sitebuilder error messaging overhaul PR
- Was looking at security scores 
- Let team know - have Thursday off
- Copy and paste, change configvalue
    - Automate selecting from dev ui what to enable on site details,
    - Update tags, change endpoint to get tags 
    - on what kind of context, group them e.g. Wishlist
## 27/03/23
- 4 of Ian’s tickets are in review in one branch.
    - Called Ian 
- Shadow Simone on site crawl
- Bimuno EN redirect
    - Natalia got back to me that she mixed up the redirect the other way round. Fixed that in live
## 28/03/23
- When reviewing Ian’s fixes I’ve noticed a small bug.
- Asked to Sit in with a go live so see if sorry server works
- Call with Ian go go over his bug fixes
- Ask catchup with Andy on the [SPIKE] I have architected a solution for BD Event Driven workflow for implementing into navigation service ticket.
    - Publish event to queue e.g. activemq, message broker, then other services can read from the queue
    - 50% done with with service. - do this for nav service. Talk with team
        - Need access
        - Big Dave client interface - already an interface for that data. Interface interpret data and push it back
        - Investigate how nav service is set up in big Dave
        - How does the endpoint in nav service work.
        - Site importer has a chrom that checks the queue already.
            - Spring annotation
        - Scope: find out a good solution for this - some in interface already, might need. A structurally similar method for services to use to 
        - If set up, hit a endpoint to report it’s done
- Started on spike ticket to architect a solution in navigation service to account for big dave’s event emitter changes
    - Investigated and updated the spike ticket on how nav service is setup from big dave’s side
- Catch up with Ali
## 29/03/23
- Cloned navigation service and will look through how on their side they set up navigation service. When that’s done, look into big Dave client interface and see what I can apply from there to a possible solution
    - Ali will shadow me for this
- Sprint planning
- On annual leave tomorrow - write up handover notes
- Started filling in hourglass for this month
## 31/03/23
- Catch up with Andy
- Finish hourglass
- Matalan trickle scripts ( 150K & 8K one) with Ali