# DevOps
A simple DevOps environment setup by docker-compose. Focus on the integration of Jira, Jenkins and GitHub.

| Component | Version | Ports |
|-|-|-|
| Nginx | 1.19.10-alpine or latest | 8080:8080, 8081:8081, 9000:9000, 50000:50000|
| Jenkins | 2.277.1-lts-alpine or latest | 8080, 50000 |
| Jira | 8.16.1 or latest | 8080 |
| Sonarqube | 8.2-community | 9000 |
| Postgresql | 9.5-alpine or latest | N/A |

# How to access
```
git clone https://github.com/Felixho19/DevOps.git
cd DevOps
docker-compose up -d
```
Then the following service can be accessed:
| Component | URL | Internal URL for configuration
|-|-|-|
| Jenkins | http://localhost:8081 | http://nginx-proxy:8081 |
| Jira | http://localhost:8081 | http://nginx-proxy:8080|
| Sonarqube | http://localhost:9000 | http://nginx-proxy:9000 |

# JIRA
Install the following plugins:
1. [Automation for JIRA](https://marketplace.atlassian.com/apps/1215460/automation-for-jira-server?hosting=server&tab=overview) 
2. [Git Integration for Jira](https://bigbrassband.com/?utm_source=Google%20search&utm_medium=cpc&utm_campaign=BigBrassBand-Prospecting&gclid=CjwKCAjw7J6EBhBDEiwA5UUM2qaXZ6oUAP0VSlELcD4qpdkjKD-W4u_TUwWuSp1erpzUYrU6zMupfRoCPmgQAvD_BwE)

# Jenkins
Install the following plugins:
1. [JIRA](https://plugins.jenkins.io/jira/)
2. [JIRA Pipeline Steps](https://plugins.jenkins.io/jira-steps/)
3. [JIRA Trigger Plugin](https://plugins.jenkins.io/jira-trigger/)
4. [JIRA ext-plugin](https://plugins.jenkins.io/jira-ext/)
5. [GitHub Pull Request Builder](https://plugins.jenkins.io/ghprb/)
