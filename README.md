SnapShot API Testing
====================
https://github.com/syrusakbary/snapshottest


Inventory API Tests
===================

 - bulk inventory create/overwrite multiple inventories happy path
 - update inventory scenarios



QA - Env in Kube
================



QA - e2e - CI
=============

 - point e2e pipeline at e2e-ci deployment

QA - Independence
=================

 - get QA dev env working on Kube
 - add setup config to Confluence
 - communicate to team


NEED HELP
=========

 - bringing down e2e, qa-dev, e2e-jenkins-spike deployments (feature_down not working) #ops
 - staging mirrored configuration (feature/values.yml - which services) to deploy to kube #ops
 - updating deployments (automating the update of deployments - after staging deploys in microservices's jenkins files) #ops #dane



Q/A
===
 Q - how do we set versions to staging in kube admin deploys?
 A - versions are set by default unless you override. Defaults get set to master/staging where appropriate

 Q - how do we keep deployments up to date with staging once deployed initially?
 A - a process of running feature_down then feature_up on the branches should update them to the latest images used on Staging
   - for now this process seemingly must be down manually

 Q - can we automate this process going foward?


