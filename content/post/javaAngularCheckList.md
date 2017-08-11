+++
date = "2017-08-10T12:00:00"
draft = false
tags = ["java", "java web applications","java checklist","checklist"]
title = "Checklist required in building Java + Angular/React App"
summary = """
I am sharing some useful checklist that are required in building java + angular/react applications.
"""

[header]
image = "checklist_java.png"
# caption = "Image credit: [**Academic**](https://github.com/gcushen/hugo-academic/)"
+++

I am sharing some useful checklist that are required in building java + angular/react applications.

**Suggestions & Feedbacks are highly appreciated.**

# Initial steps

- Finalize tech stack
- Create a multi-module Maven or Gradle project. I recommend to start with two modules, one which contains front-end code like angular/react and back-end which contains java code.
- Use Maven or Gradle wrapper scripts so that there is no need to install Maven or Gradle on the machine before executing the build.
- Build project as a single jar/war file using a single command. If it is a maven project you should able to run `./mvnw clean install` in the project root to build the executable.
- Set up a Continuous Integration server and make sure it can build the project as a single executable.

# [Git](http://nvie.com/posts/a-successful-git-branching-model/)

- Work on feature branches.
- Branch out from `develop` branch.
- Never push to `master` or `develop`. Make a pull request.
- Create pull request on the `develop` and once it is tested then only merge to master. You can use different stratergy like merge to `master` once sprint finishes.
- Delete local and remote branches after merging. You can automate this process as well.
- Before raising pull request, run the build locally and make sure all tests pass.
- Use `.gitignore` file.
- Protect your master branch.
- Never commit binary files to Git.
- Write meaningful Git commits messages. [How to Write a Git Commit Message-- Chris Beams](https://chris.beams.io/posts/git-commit/)
- Feature branches should be short lived.

# Dependencies

- Add a new dependencies to the project after discussing with the team.
- Use [Snyk](https://snyk.io/) to check security vulnerabilities.
- Don't add dependency for each problem you face. First check if you already have some dependency that solves the problem.

# Code style

- For backend, use [Checkstyle](http://checkstyle.sourceforge.net/) in your project. Make sure you it is integrated with the build.
- For frontend, use ```ESLint``` or ```TSLint```.

# [CI](https://martinfowler.com/articles/continuousIntegration.html)

- Every code committed to version control system mainline should trigger a continuous integration job that runs on the integration server.
- Continuous integration job should build the project and run all unit test cases. It should happen on each code commit to mainline.
- Fix broken builds immediately. CI server should always be in healthy green state.
- Make CI server visible and transparent to whole team.
- Maintain build jobs as code use Jenkinsfile if you are using Jenkins.
- You should be able to create build jobs on a new CI server using code.
- Use pull request builder to build the project when pull request is raised.

# [Documentation](https://robots.thoughtbot.com/how-to-write-a-great-readme)

- Create `README.md` file in root of your project and keep it updated. The README file should have following
- Couple of lines describing purpose of the project.
- Instruction to grab the latest code and detailed instructions to build it.
- Instructions to run the project on local machine.
- Link to Continuous integration server.
- Instruction to do any setup required for the project.
- Instruction to grab project documentation.
- Any other relevant information that can help a new developer get started with the project.

# Testing

- Write one automated functional test per user story.
- Cover business logic with unit/Integration tests.
- Understand different between unit testing and integration testing.
- Use consistent names for tests.

# Naming

- Think and discuss with team before choosing a name for public member.
- Java and JavaScript use ```PascalCase``` for classes, interfaces, enums, annotations.
- Java and JavaScript use ```camelCase``` for methods and variables.

# Exception handling

- Catch any checked exception thrown by the code.
- Convert checked exceptions to unchecked exceptions.
- Throw the unchecked exception. Unchecked exceptions could be couston or plain RuntimeExeception.
- Always use two argument constructor of RuntimeException. The fist take a message, second is the actual exception.
- Catch all exceptions thrown by code in your controller and resource classes.
- Log exceptions only in the controller or resource classes.
- Log both the message and exception.

# Rest API Design

- selection of resources is to analyze your business domain and extract the nouns that are relevant to your business needs.
- Do not use `GET` for state changes.
- Do not mix up singular and plural nouns. Keep it simple and use only plural nouns for all resources.
- If a resource is related to another resource use subresources.
- Both client and server need to know which format is used for the communication. The format has to be specified in the HTTP-Header.
- ```HATEOAS``` (**Hypermedia as the Engine of Application State**) is used to create a better navigation through the API's.
- Allow ascending and descending sorting over multiple fields.
- All exceptions should be mapped in an error payload.

# Logging

- Use slf4j for logging.

# [Code Review](https://www.atlassian.com/agile/code-reviews)

**Code reviews are about code not people. Don't take code criticism personally.**

- Are there any obvious logic errors in the code?
- Are unit tests written for the business logic?
- Does all the functional requirements met?
- Does the code conform to existing style guidelines?
- Propose better way to do certain tasks. It could be a library function that developer can use.
