# CICD
Architecture designs and evolving

## Code Analysis at http://localhost:9000/ admin default
1. install postgresql
  * create schema and user
  CREATE USER sonarqube PASSWORD 'sonarqube'
  CREATE DATABASE sonarqube WITH OWNER = sonarqube ENCODING = 'UTF8' LC_COLLATE = 'English_United States.1252' LC_CTYPE = 'English_United States.1252'
  ALTER USER sonarqube SET search_path to public
2. Installing the Web Server http://docs.sonarqube.org/display/SONAR/Installing+the+Server
  * setting jdbc C:\java\sonarqube-4.5.6\conf\sonar.properties
  sonar.jdbc.username=sonarqube
  sonar.jdbc.password=sonarqube
  sonar.jdbc.url=jdbc:postgresql://localhost/sonar
3. Analyzing with SonarQube Scanner
  * C:\java\sonar-scanner-2.5\conf\sonar-runner.properties
  sonar.host.url=http://localhost:9000 and db
  * SONAR_RUNNER_HOME=C:\java\sonar-scanner-2.5
  * path = C:\java\sonar-scanner-2.5\bin
  * go to folder add sonar-project.properties and run sonar-runner  
4. Config sonar-project.properties  
sonar.projectKey=ionic  
sonar.projectName=JavaScript HTML CSS:: SonarQube Scanner 
sonar.projectVersion=1.1.1 
sonar.sourceEncoding=UTF-8 
sonar.sources=www 
sonar.exclusions=www/lib/** 
