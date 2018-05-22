CURRENT WORK
=============

Integrations - Assortment Export
--------------------------------

### send success email

#### questions

  1. How can we determine number of assortments exported? How are we splitting out the assortments in export?
  1. How much can we make use of integrations_mailers previously written by jyeo?
  1. When are we sending this email? (after output of file, after brickftp transfer?)

##### How much can we make use of integrations_mailers previously written by jyeo?
  - quite a bit, need to create a class that inherits from integrations.email.common.IntegrationMailer
  - class would override get_body() and get_subject() methods and send in assortment_export stats into self.send_data mailer_class.send(data={assortment_exports: ...})






### Working with data on staging db on local
 1. dump staging data to local
 1. copy certain tables with postgres copy command to files
 1. use SCP (secure copy) to copy files from foreign server to local
