# Site Details Running Instructions
## Terminal 1
1. java17 || export JAVA_HOME=`/usr/libexec/java_home -v 17`
2. nvm use
3. yarn
4. ./gradlew run -PonlyIncludeModules={module names}
   - ./gradlew run -PonlyIncludeModules=com.thg.teepee.sitedetails.ui 
5. Site Details should be accessible on http://localhost:8090/
## (To auto-build when changes made) Terminal 2:
1. cd {module you changed}/app
2. ng build --watch