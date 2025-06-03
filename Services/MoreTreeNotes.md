### Personal Okta 1TP order
1. UAT
2. Live
3. Dev

## MORETREES:
### Setting up mt locally
- Ui
  - Nvm use 22
  - Npm install
  - Disable Cloudflare, npm run dev, enable Cloudflare to login
- User
  - Clone mt-common, java 17, mvn clean install
  - Add environment variables in configuration for main, Cd environment, docker-compose up -d, cd ../, java17, mvn clean install
- DB access
  - conductorOne request resources strongdm eco-nonprod and eco-prod, to approve, go under tasks of app.
  - Switch from public view to mt-users schema (bottom left)
- transaction: when installing, 
  - Add more trees stuff to ~/.m2/settings.xml
- Project: when running, can’t find package openapi.model. need restarting intelliJ fully
  - Working
### For help: 
- jack king (general Qs), jack Owen (code)
### Pulling data process
- Comes in monthly: monthly commercial report in confluence. Update dates for previous month.
- PII : personal identification. Apply expiration date and only link share to specific people. Add password 
- Transaction type code in thg common
- Account type I is individual, C is business/company
### Customer delete account process
    - Come from DL-MoreTreesTech 
    - Email address linked to one user, but one user can be linked to multiple accounts
    - Queries in more trees confluence. How to: close customer account.
- When select account invitations, set to complete if any turn ups     
- Mt_user.account_users close all
- Add deleted code in mt_user.countries and update UI so users cannot select deleted country option. Look into relying on status value
- Go to auth0, switch to prod, go to users, and delete user using email
### Ask about certification expiry ping
- Contact app runtime support channel about expired certificate
### Ask about mt down ping
- Confluence documentation exists about it
