CURRENT WORK
=============

# Update Inventory API Tests

### current problem we're dealing with:
we're trying to create one new inventory and update another inventory, while soft-deleting a third

#### current behavior:
 1. overwrite "updates" inventories included in request by CREATING new inventory records and SOFT-DELETING the old ones
 1. It does NOT "soft delete" inventory_item records not included in request. It leaves those not included in the request alone.
 1. It performs this "overwrite" update by creating a new inventory_item and linking that to a new inventory record, while setting prior inventory_item to "soft deleted"

##### oddities - problem 1:
 1. it seems that the new inventory records created during "overwrite" to update old ones are ALSO being SOFT-DELETED (set to deleted=True)
 1. it seems a TON of inventory_item records are suddenly created right after the test run but before cleaning (??? - wtf?!)

##### made to order - problem 2:
 from documentation:
   "If using the Overwrite setting, you can set a style to be "Made to Order" by not including it in your next load"

  - this actually seems to be working as expected currently

