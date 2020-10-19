
# team-a-jenkins-config

This repo contain configuration file for team-a jenkins instance. for any changes in plugins or configuration this this repo should be updated. 

## Steps to update the plugin.
1. Update vaules.yaml with new plugin.

```
  installPlugins:
    - newplugin:x.x
```

2. Retrigger onboarding jenkinsfile or if you have access to the cluster then execute below commands.

```
git clone https://github.com/letscode-ss/team-a-jenkins-config
git clone https://github.com/letscode-ss/4-devops-with-jenkins.git
helm upgrade --install jenkins-<namespace> --values team-a-jenkins-config/values.yaml 4-devops-with-jenkins.git/charts/jenkins/
```
