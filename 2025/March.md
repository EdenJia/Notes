## 03/03/2025
- Site info data matchup with sitecreatedevent
## 04/03/2025
- Finish backfill process
- Pick up site ownership ticket for site info api
    - Contacted sam
    - Can’t connect to pl Elysium
## 05/03/2025
- Continued with site ownership ticket
    - Crafted sql statements, tested in ST
    - Making codebase changes
    - Readying PR
    - Call with Ian
## 06/03/2025
- Fixing warehouseIds SQL
## 07/03/2025
- Continue with site info api fix
    - Export new table data in PL
    - Unzip, remove comments and rep
    - Replace in localdev/sql dir
    - Typescript change testing for pulling warehouseIds
    - Try to pre-release again to ST
## 08/03/2025
- Sick leave
## 10/03/2025
- Continue with bug fix
    - DB and codebase issue
    - Create new ticket for this bug in backlog
- Call with Ian
- Call with Ihor
    - Demo redirect manager api
## 11/03/2025
- Fixed site info api parsing bug fix
- Call with Ian to test run ARES locally
    - Change .env.list to .env.dist
## 12/03/2025
- Retro sprint planning
- Appeal with FWR meeting
- Nav service EDA auth integration
- firefighting
## 13/03/2025
- Nav service eda auth integration
- Nav service pl bug fix
## 14/03/2025
- Nav service pl bug fix
- Update and delete endpoint in redirect api
    - Migrated the related validation from apollo to separate class
## 17/03/2025
- Nav service pl bug fix
    - Review and release
- Update and delete endpoint in redirect api
    - Migrated the related validation from apollo to separate class
## 18/03/2025
- Nav service release to live and monitoring
- Security update
## 19/03/2025
- Continue with redirect api
    - Reviewed by ihor and released
## 20/03/2025
- Pick up health check ticket
    - Followed James’ comment about creating a rest endpoint for a health check. Running into build errors with online documentation being no help even with the version of apolloserver the project’s on.
## 21/03/2025
- Pre-released site info api to hell and back
    - Finished
## 24/03/2025
- Site info api query ticket 
- Engineering meeting
    - Ian attempted to migrate bigdave api from tcp to ssl but encountered helm upgrade issues on the pipeline Friday evening. He’s not feeling well today. My priority today to release that
    - Johnny working on zapier integration
- Rollback
    - In ns, helm ls -a, helm rollback <name in ls>
        - Failed
    - Apply
## 25/03/2025
- Feed manager Eda auth integration
    - Already completed by checkout
- Country manager Eda ate integration
    - Already completed by checkout 
- Review services Eda auth integration
    - Done by engagement as well
- SLS auth integration - done as well
- Created tickets for redirect api
- Started ticket on site info api documentation in backlog
## 26/03/2025
- Continue documentation, in review 
- Eda auth tickets added relevant PRs
    - 4 of them. Released  
- Redirect api endpoints
    - 9 to do
    - Did 4, need to test
- Feed manager consumeSiteCreatedEvent missing validation
    - Asked for write permission
- Sitebuilder service configs missing feed manager and channel manager/region group
    - Exist in sitebuilder test/generate.ts
## 30-31/03/2025
- Continue PR for feed manager
- EDA fix for country manager
    - Released to ST, forgot to ask messaging team to allow queue name creation in CT, waiting on them