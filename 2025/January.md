## 02/01/2025
- Sprint planning
- Helped unblock a task James was on
- Helped Ian with logging onto the bdsa GitHub account
- Updated documentation regarding ^
- Get in touch with eCRM for help in setting up their config service
    - Email sent
    - Ali lmk that when he was working with ecrm that: when i made my changes etc Stephen deployed it to test them
## 03/01/2025
- Obfuscate secrets with James’ Apollo PR as template
    - Call with James
- Call with ian found error w/ Olympus change. Talk to Ihor about httpstatuscodeexcption not catching 404 notfoundexception error
- Contact messaging team about live password issues
    - resolved
- Jurgita confirms VT visibility on AMQ UI in planning next week
- Navigation service event integration problems in PL but not in Live
- Ihor Qs: Olympus httpstatuscodexception confusion
## 06/01/2025
- Get Olympus running to test new code
    - Running, not testing yet.
- Follow up with eCRM, Stephen lewis back
    - Stephen just asked for changes to be made and pushed without me testing it since it’s a one line change
    - Merged but had issues deploying to ST, using a bigdaveclientinterface version that doesn’t exist. I fixed it
- Completed mandatory training course
## 07/01/2025
- Test Olympus
    - Not running again
- eCRM credentials: Stephen contacted people on the rocky team to do this as he doesn’t know how
## 08/01/2025
- Ask Ian to test my new code on Olympus, fixed
    - Ian has been given write access to Olympus
- Check up on eCRM team with integrating THG-IET org
    - Had to log into their SA account but failed, one lost access to their 1password.
    - Asked to be added to THG-IET, so I asked which one, Okta or GitHub. Okta needed to be done first, so I supported in that area - they made a ticket and is waiting to be picked up.
## 09/01/2025
- eCRM support
    * Managed to set the token, but still not working. Still trying to fix on their end
    * Tested on different settings.xml, one with credential works. Otherwise same error as runner
- Ask navigation service team on PL vs Live behaviour, and messaging team whether credentials are now implemented in PL
    - Investigated UI and no consumer on PL, 12 consumers on gb1-li-coreplatform, 12 on gb4-li-coreplatform
    - Last Navigation service log on PL and Live bigdave DB is for site id 388 us February 15 2024
    - Activemq password added to nav service 18/10/2024 Maisie Johnson
    - Last franked subsite in sitebuilder is Wellbeloved D2C DE where nav service is not set up https://sitebuilder.io.thehut.local/subsite/cf2e586b-05c1-4612-bb98-09eacff4dfaa/service-configurations
    - ^ Upload id: cf2e586b-05c1-4612-bb98-09eacff4dfaa can’t find in bigdave PL DB
## 10/01/2025
- Continue nav service investigation
    - Chased nav service - no response
- eCRM support
    - No response from Stephen lewis
- Hr asked for more details about flexible working requirements. Responding to that
## 13/01/2025
- Chase nav service
- Chase Stephen lewis 
    - He believes the github runner is running out of memory, causing the package to fail to be pull. Trying to set that up
## 14/01/2025
- Test release bigdave for amq secrets pulling in correctly
    - Live password is using ‘fakepass’
- Chase nav service
- Chase Stephen lewis
## 15/01/2025
- Supercharged engineering meeting
- Retro & planning
- Stephen lewis: add Ian Parkinson to gc for visibility
    - Stephen added Ryan king. Ryan king fixed it and deployed to UAT. Asked to deploy to PL to test as well. Kept contacting me via DM and not via gc.
- Chase nav service in general thread of platform content (parked until next sprint)
- Call Ihor to ask about live amq password inconsistencies in bigdave
    - Messaging team contact live password issue
## 16/01/2025
- BRP meeting
- Test eCRM ST AMQ release
- Bigdave live password issues messaging team
    - Amq Connection labelled ‘live’ in the application is only true if its current environment is live.
    - Karolis Dzekunskas messaged - turned out password was wrong and gave me the correct one.
    - Deleted commit where I committed the passwords from branch and rebased
- Site info api
## 17/01/2025
- Get big Dave review fixed and release
## 20/01/2025
- Asking for final review from Ihor and Get Big Dave released on PL and tested. 
- Infractl dc login problems
## 21/01/2025
- Release bigdave to live and check logs
- DC password reset via 3 way meeting between Ihor, me and a technician
## 22/01/2025
- Do self review
- Ryan Jackson reached out for a review on big Dave
    - Update teepee urls because of the split to thgingenuity
    - Released now
## 23/01/2025
- Fill out self review form
- 1password issues
## 24/01/2025
- 1password recovery
- Looked at other redirect tickets
    - Redirect ticket on oral B 
        - Several have query source exceeded char limit of 350
        - Other redirects have been inserted
        - Alerted Connor harper on this. Waiting for his testing and additional support if needed
    - Fuel10k, no movement for 5 months. Set as done
    - Protexinpet US closed off, Simone has left a comment to look into it but has since left. I picked up investigation, found redirect requested now exists, asked SEO to confirm and they’re happy with it
## 27/01/25
- Look at apollo/prop service docker pr as template, apply to other services apply to bigdave
- Updating Cloudflare to java home, npm, git, intelliJ, vscode
## 28/01/25
- Apollo amq
    - Needs to run with Cloudflare off otherwise timeout
    - Tomcat issues
- Flex meeting: 18th February
- Assist ihor release sorry server, site importer api (runner issues), redirect engine and properties service
    - Properties service has a lot of merged prs that haven’t been released:
* What's Changed
* Introduce custom ingress controller by @jameshealythg in #37
* increasing loadtest traffic by @harrietg24 in #39
* Set disruption budget by @jameshealythg in #40
* Updating Cloudflare Certificate by @jameshealythg in #41
        - Prop service, redirect engine and sorry server deployed
## 29/01/25
- Thg hourglass
- Properties service AMQ PR
- Context regarding artifactory ticket. What are we migrating to?
    - To GitHub packages
    - deadline: check group_technology from jo drake
## 30/01/25
- Prop service amq release: parked for ecrm
- Retro
- Update macOS
- Ecrm update: deployed to st and uat. Checked UIs and consumers are on the right queues. Need full pipeline testing
    - Call with Ian with testing ecrm
        - Failed to convey him how amq topics and queues work
    - Messages are. Enqueued and dequeued correctly but no service configured event sent back to big Dave
    - Think subsites we’re trying are already set up in ecrm config service. Need ecrm team to check which ones are configured
- Link Olympus Eda ticket to the Olympus James ticket
- Clarify testing for apollo amq auth PR to James
## 31/01/2025
- Release properties service
    - Missed adding secret to k8 gb1 and gb4 deployment step in deployment.yaml - fixed