QA - e2e - CI
=============

 1.- fix migrations for CI setup locally
 2.- run successful unscheduled e2e pipeline build
 3.- schedule runs
 4.- integration with slack messages on failures

QA - Independence
=================

 - get QA dev env working on Kube
 6. - add setup config to Confluence
 7. - communicate to team

##QA - Env in Kube

 5.- test QA-dev deployment running slimmed down dev env setup locally


NEED HELP
=========

### feature_down
 - bringing down e2e, qa-dev, e2e-jenkins-spike deployments (feature_down not working) *#ops*

### migrations
 - migrations, django migrations need to be run *#ops*

### feature_up (mirror staging and auto deploys)
 - staging mirrored configuration (feature/values.yml - which services) to deploy to kube *#ops*
 - updating deployments (automating the update of deployments - after staging deploys in microservices's jenkins files) *#ops* *#dane*


Q/A
===
 Q - how do we set versions to staging in kube admin deploys?
 A - versions are set by default unless you override. Defaults get set to master/staging where appropriate

 Q - how do we keep deployments up to date with staging once deployed initially?
 A - a process of running feature_down then feature_up on the branches should update them to the latest images used on Staging
   - for now this process seemingly must be down manually

 Q - can we automate this process going foward?


Inventory API Tests
===================

 - bulk inventory create/overwrite multiple inventories happy path
 - update inventory scenarios


SnapShot API Testing
====================
https://github.com/syrusakbary/snapshottest


