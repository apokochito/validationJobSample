# validationJobSample

Java development with Jenkins Job configuration.

This validation job needs to execute and validate a successful flow of data of the following project structure.

### Project Structure

- FrontendSample // https://github.com/apokochito/frontendSample
- BackendSample // https://github.com/apokochito/backendSample
- SecuritySample // https://github.com/apokochito/securitySample
- ValidationJobSample // This repository

### Process

#### Jenkins configuration (not necessary)

Installation steps (by windows option)

- Download Jenkins from https://www.jenkins.io/download/#downloading-jenkins
- Run service as LocalSystem (not recommended)
- Configure port Number 9040 and open chrome using http://localhost:9040
- Set local system password
- Plugins nstallation process...
- Create admin user
- Instance configuration with (http://localhost:9040)

Installation steps (by Docker option)
- PENDIENT

Validation Job Creation

- From home page, select "New Item" and name it as ValidationJob
- Select "Pipeline" type
- In General section select "This project is parameterized"
- Add "String Parameter" as...

	- Name as "ENVIRONMENT"
	- Default value as "dev"
	- Description as
		
		dev
		
		dev-stage

- Add the link to your Github Project "this repo url"
- Add shell command... sh "mvn clean test -P $ENVIRONMENT -U -DskipTests=false"

