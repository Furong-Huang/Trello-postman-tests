# Trello-postman-tests

Running a Trello collection from a Git repository with Jenkins

It also need to register Trello account in order to get trelloKey and trelloToken which can be set in environement variables.

Configurate Jenkin:
Source Code Management: choose Git and paste https://github.com/Furong-Huang/Trello-postman-tests.git in Repository URL
Branch Specifier (blank for 'any'): */main

Executed Windows batch command:
newman run "My Trello.postman_collection.json" --disable-unicode --environment "Trello Env.postman_environment.json" --reporters cli,junit,html --reporter-json-export "newman/report.xml" --reporter-html-export "newman/report.html"

