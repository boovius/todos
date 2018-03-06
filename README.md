QA - e2e - CI
=============

 1. integration with slack messages on failures
 2. script up moving forward with CI - automation on staging deploys

QA - Independence
=================


NEED HELP
=========

### feature_down
 - bringing down e2e, qa-dev, e2e-jenkins-spike deployments (feature_down not working) *#ops*

### migrations
 - migrations, django migrations need to be run *#ops* (ops working on it currently 3/6/18)

### feature_up (mirror staging and auto deploys)
 - staging mirrored configuration (feature/values.yml - which services) to deploy to kube *#ops*
 - updating deployments (automating the update of deployments - after staging deploys in microservices's jenkins files) *#ops* *#dane*


Updates and Nice to Haves
=========================

 - set WEB_URL env variable by default when doing j_start_e2e to http://www


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


