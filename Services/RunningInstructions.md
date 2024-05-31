# SITE AUTOMATION PRODUCT RUNNING INSTRUCTIONS

## MODULAR TEEPEE:

Terminal 1:
```
export JAVA_HOME=`/usr/libexec/java_home -v 17

nvm use, yarn

./gradlew run -PonlyIncludeModules={module names}

./gradlew run -PonlyIncludeModules=com.thg.teepee.sitedetails.ui, ./gradlew run -PonlyIncludeModules=com.thg.teepee.sitedetails.ui,com.thg.teepee.sitedetails.provider.sitedetailsservice,com.thg.teepee.sitedetails.dto,com.thg.teepee.sitedetails.domain,com.thg.teepee.sitedetails.api,com.thg.teepee.sitedetails.provider.mock
```
Modular Teepee should be accessible on `http://localhost:8090/`
```
ng test --code-coverage to run tests, open web/coverage/index.html in browser to view report
```
(To auto-build when changes made) Terminal 2:
```
cd {module you changed}/app
ng build --watch
```

## SITEBUILDER NXT
```
export JAVA_HOME=`/usr/libexec/java_home -v 11

nvm use, yarn

yarn dev:server / 
```
to run tests
```
yarn test:e2e
``` 
to update sonarqube page with new changes in your branch
``` 
yarn run sonar 
``` 
Sitebuilder should be accessible on `http://localhost:3000/`

To run cypress tests, 
```
run npx cypress open
```
 
## Big Dave

Open in IntelliJ
```
export JAVA_HOME=`/usr/libexec/java_home -v 11
```
Check in `Edit Configuration` that the profile is set as `dev`
Click the play button to build and run

BD should be accessible on `http://localhost:8085/`

## PROPERTIES SERVICE
Moved to ModTP

## CHECKOUT
```
sudo spctl --master-disable to allow chromedriver-mac to run

podman machine start, podman start activemq, open couchbase
```
On IntelliJ, run proxy, then JS build + watch, then mockAdapter, then checkoutAPIApp, then checkout and then start a checkout session

To take screenshots for PR: https://chrome.google.com/webstore/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl

## SITE IMPORTER API
```
cd localmssql, 
podman machine start, podman build -f mssql.Dockerfile -t siteimporter && podman-compose up -d 
```
If you don't have an mssql server connection on your DB management app e.g. Tableplus, create this connection:

Name: SiteImport-Local, Host: localhost, Port: 7892, User: sa, Password: Password789!
Test connection & if successfuly, connect
Copy the whole file from localmssql/initialsetup/setup.sql, paste into the DB management app and run the first line to create the siteimporter database
Remove the GO statements and run the rest of the setup.sql
If you don't have a spring boot run configuration, create one

Select the main class as com.thehutgroup.siteimporter.Application
Select the module classpath as siteimporter.server.main
Select the correct JRE, Java Version 11.
In the Active Profiles field, type in dev.
Run the run configuration!

## SLS
```
docker login to ghcr.io/thg-engagement/rockylinux-jdk-17 (github username & token)
docker login artifactory.io.thehut.local:5000/engagement-vertical/flyway (DC account)
./gradlew clean assemble to check build, then ./gradlew startDocker
```
## Navigation Service
```
./gradlew clean spark:assemble -Djavax.net.ssl.trustStore="/Users/edenjia/Downloads/cacerts" -Djavax.net.ssl.trustStorePassword=changeit
```
## Olympus
1. `git clone` olympus, 
2. replace `.m2/settings.xml `with {insert file here}, 
3. app needs node 16 and java 11, 
4. comment line 16 in `applications-dev.properties` to allow lazy startup, 
5. `mvn install`, 
6. `sudo npm install —legacy-peer-deps`, 
7. `sudo npm install webpack-plugin --legacy-peer-deps`
8. `sudo npm run build`, 
9. then run olympusApplication config from intellij - to setup and run Olympus 