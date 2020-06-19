--- 

title: Yellow Dog Fetch API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

This is the fetch api for 3rd Party integrations to Yellow Dog Inventory. For authentication documentation and examples go to https://yellowdogsoftware.github.io/fetch-api. 

**Version:** v0.33.0 

# /API/V{APIVERSION}/ACCOUNTING/{STOREID}/{DATE}/RETURNTOVENDORS
## ***GET*** 

**Summary:** Returns a listing of Return to Vendors based on store

### HTTP Request 
`***GET*** /api/v{apiVersion}/accounting/{storeId}/{date}/returnToVendors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path | Id of the store that is being fetched | Yes |  |
| date | path | Date String in the local time of the database server | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ACCOUNTING/{STOREID}/{DATE}/INVOICES
## ***GET*** 

**Summary:** 

### HTTP Request 
`***GET*** /api/v{apiVersion}/accounting/{storeId}/{date}/invoices` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path | Id of the store that is being fetched | Yes |  |
| date | path | Date String in the local time of the database server | Yes |  |
| nonPrepaidOnly | query |  | No |  |
| includeReceipts | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ACCOUNTING/{STOREID}/{DATE}/REVENUE
## ***GET*** 

**Summary:** 

### HTTP Request 
`***GET*** /api/v{apiVersion}/accounting/{storeId}/{date}/revenue` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path | Id of the store that is being fetched | Yes |  |
| date | path | Date String in the local time of the database server | Yes |  |
| types | query | Choose one or more of the following Journal Entry types (Sale, Tax, Tender) | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ACCOUNTING/{STOREID}/{DATE}/JOURNALENTRY
## ***GET*** 

**Summary:** 

### HTTP Request 
`***GET*** /api/v{apiVersion}/accounting/{storeId}/{date}/journalEntry` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path | Id of the store that is being fetched | Yes |  |
| date | path | Date String in the local time of the database server | Yes |  |
| types | query | Choose one or more of the following Journal Entry types (PhysicalInventory, ManualAdjustment, CostOfGoodsSold, Transfer, Receipt) | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ACCOUNTING/{STOREID}/CODES/{CODETYPE}
## ***GET*** 

**Summary:** Gets a listing of accounts and their code data

### HTTP Request 
`***GET*** /api/v{apiVersion}/accounting/{storeId}/codes/{codeType}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path | Id of the store that is being fetched | Yes |  |
| codeType | query | Type of account | No |  |
| apiVersion | path |  | Yes |  |
| codeType | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ATTACHEDFILES/{ID}
## ***GET*** 

**Summary:** Gets image based on Id. This image can be associated to an Item or a Recipe.

### HTTP Request 
`***GET*** /api/v{apiVersion}/attachedFiles/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | AttachedFile Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/COUNTSHEETS
## ***GET*** 

**Summary:** Getting Count Sheets

### HTTP Request 
`***GET*** /api/v{apiVersion}/countsheets` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/COUNTSHEETS/{ID}
## ***GET*** 

**Summary:** Getting a Count Sheet by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/countsheets/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CountSheet Id | Yes |  |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/CURRENCY
## ***GET*** 

**Summary:** Getting Currency

### HTTP Request 
`***GET*** /api/v{apiVersion}/currency` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - currencyCode  - date  - exchangeRate  - lastUpdated | No |  |
| OrderBy | query | ### Order By Options:  - currencyCode  - date  - lastUpdated | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creating new Currency Exchange Rate

### HTTP Request 
`***POST*** /api/v{apiVersion}/currency` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PUT*** 

**Summary:** Updating existing Currency Exchange Rate

### HTTP Request 
`***PUT*** /api/v{apiVersion}/currency` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Bulk delete Currency Exchange Rates

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/currency` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/CURRENCY/EFFECTIVEEXCHANGERATE/{CURRENCYCODE}
## ***GET*** 

**Summary:** Getting Currency by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/currency/effectiveExchangeRate/{currencyCode}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| currencyCode | path |  | Yes |  |
| date | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/CURRENCY/{ID}
## ***GET*** 

**Summary:** Getting Currency by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/currency/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Deleting a Currency Exchange Rate

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/currency/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/DIMENSIONS
## ***GET*** 

**Summary:** Getting Dimensions

### HTTP Request 
`***GET*** /api/v{apiVersion}/dimensions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creating new Dimensions

### HTTP Request 
`***POST*** /api/v{apiVersion}/dimensions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PUT*** 

**Summary:** Updating existing Dimensions

### HTTP Request 
`***PUT*** /api/v{apiVersion}/dimensions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/DIMENSIONS/{ID}
## ***GET*** 

**Summary:** Getting Dimension by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/dimensions/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Dimension Id | Yes |  |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Deleting a Dimension

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/dimensions/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Dimension Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/FLAGS
## ***GET*** 

**Summary:** Getting Flags

### HTTP Request 
`***GET*** /api/v{apiVersion}/flags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/FLAGS/{ID}
## ***GET*** 

**Summary:** Getting Flag by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/flags/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Flag Id | Yes |  |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/INVENTORY
## ***POST*** 

**Summary:** Gets all Inventory

### HTTP Request 
`***POST*** /api/v{apiVersion}/inventory` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMALIASES
## ***POST*** 

**Summary:** Adding Item Aliases

### HTTP Request 
`***POST*** /api/v{apiVersion}/itemaliases` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS
## ***GET*** 

**Summary:** Gets all Items

### HTTP Request 
`***GET*** /api/v{apiVersion}/items` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - active  - lastUpdated  - levelId  - sku | No |  |
| Expand | query | ### Expand Options:  - stores  - vendors  - images (available on database versions above 366) | No |  |
| OrderBy | query | ### Order By Options:  - sku  - description  - itemId | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS/{ID}
## ***GET*** 

**Summary:** Gets an Item by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/items/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes |  |
| Filter | query | ### Filter Options:  - active  - lastUpdated  - levelId  - sku | No |  |
| Expand | query | ### Expand Options:  - stores  - vendors  - images (available on database versions above 366) | No |  |
| OrderBy | query | ### Order By Options:  - sku  - description  - itemId | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS/{ITEMID}/IMAGES
## ***POST*** 

**Summary:** Adds an Image as an Attached File to an Item.

User's client *MUST* be 366+ with cloud storage enabled

### HTTP Request 
`***POST*** /api/v{apiVersion}/items/{itemId}/images` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | Item Id | Yes |  |
| description | query | Description or Title of the Image file | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS/{ITEMID}/ADDIMAGE
## ***POST*** 

**Summary:** Adds an Image as an Attached File to an Item

User's client *MUST* be 366+ with cloud storage enabled

### HTTP Request 
`***POST*** /api/v{apiVersion}/items/{itemId}/addImage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | Item Id | Yes |  |
| description | query | Description or Title of the Image file | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS/{ITEMID}/IMAGES/{IMAGEID}
## ***DELETE*** 

**Summary:** Deletes an item's image

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/items/{itemId}/images/{imageId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | Item Id | Yes |  |
| imageId | path | Attached File Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PATCH*** 

**Summary:** Updates the Description of an Items Attached File

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/items/{itemId}/images/{imageId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| itemId | path | Item Id | Yes |  |
| imageId | path | Attached File Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/ITEMS/{ID}/RETAILS
## ***POST*** 

**Summary:** Adds a new record for an item's retail

### HTTP Request 
`***POST*** /api/v{apiVersion}/items/{id}/retails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Item Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/MANUALADJUSTS
## ***POST*** 

**Summary:** Creates Manual Adjustments

### HTTP Request 
`***POST*** /api/v{apiVersion}/manualadjusts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/METAINFO
## ***GET*** 

**Summary:** Get all Meta Information for YDI Interface

**Description:** In Yellow Dog the user is able to configure the Names that are used on buttons to make the user interface more friendly for their particular use. This endpoint will display the values of these name changes.

Common examples of this are:
- Dimension 1 is named Size in the Yellow Dog Interface, Dimension 1 (Size) will be index 0 of the dimensions array.
- Flag is named Location

### HTTP Request 
`***GET*** /api/v{apiVersion}/metainfo` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/{ID}/REQUESTTIEREDAPPROVAL
## ***POST*** 

**Summary:** Starts the process of Tiered Purchase Order Approval process

### HTTP Request 
`***POST*** /api/v{apiVersion}/purchaseOrders/{id}/requestTieredApproval` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Purchase Order | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/TIEREDAPPROVAL
## ***PUT*** 

**Summary:** Approves a Purchase Order Tier

### HTTP Request 
`***PUT*** /api/v{apiVersion}/purchaseOrders/tieredApproval` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS
## ***GET*** 

**Summary:** Gets Purchase Orders

### HTTP Request 
`***GET*** /api/v{apiVersion}/purchaseOrders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - docNumber  - committed  - lastUpdated  - vendor | No |  |
| Expand | query | ### Expand Options:  - Items  - Stores  - Users  - Vendors  - LineDetails  - ApprovalStatuses | No |  |
| OrderBy | query | ### Order By Options:  - committed  - docNumber  - lastUpdated | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creates Purchase Orders.

### HTTP Request 
`***POST*** /api/v{apiVersion}/purchaseOrders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/{ID}
## ***GET*** 

**Summary:** Get Purchase Order by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/purchaseOrders/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Purchase Order | Yes |  |
| Expand | query | ### Expand Options:  - Items  - Stores  - Users  - Vendors  - LineDetails  - ApprovalStatuses | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/BYTOKEN
## ***GET*** 

**Summary:** Get Purchase Order by token

### HTTP Request 
`***GET*** /api/v{apiVersion}/purchaseOrders/byToken` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query | ### Expand Options:  - Items  - Stores  - Users  - Vendors  - LineDetails  - ApprovalStatuses | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/{ID}/APPROVALSTATUS
## ***GET*** 

**Summary:** Get Purchase Order Approval Status by Id of Purchase Order

### HTTP Request 
`***GET*** /api/v{apiVersion}/purchaseOrders/{id}/approvalStatus` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Purchase Order | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/PURCHASEORDERS/APPROVALSTATUSBYTOKEN
## ***GET*** 

**Summary:** Get Purchase Order Approval Status using token

### HTTP Request 
`***GET*** /api/v{apiVersion}/purchaseOrders/approvalStatusByToken` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/RECEIPTS
## ***GET*** 

**Summary:** Gets Receipts

### HTTP Request 
`***GET*** /api/v{apiVersion}/receipts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - docNumber  - committed  - lastUpdated  - vendor | No |  |
| Expand | query | ### Expand Options:  - Items  - Stores  - Users  - Vendors | No |  |
| OrderBy | query | ### Order By Options:  - committed  - docNumber  - lastUpdated | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/RECEIPTS/{ID}
## ***GET*** 

**Summary:** Get Receipt by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/receipts/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Id of Receipt | Yes |  |
| Expand | query | ### Expand Options:  - Items  - Stores  - Users  - Vendors | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/RECIPES/{RECIPEID}/IMAGES
## ***POST*** 

**Summary:** Adds an Image as an Attached File to a recipe

User's client *MUST* be 366+ with cloud storage enabled

### HTTP Request 
`***POST*** /api/v{apiVersion}/recipes/{recipeId}/images` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| recipeId | path |  | Yes |  |
| description | query | Description or Title of the Image file | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/RECIPES/{RECIPEID}/IMAGES/{IMAGEID}
## ***DELETE*** 

**Summary:** Deletes a recipe's image

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/recipes/{recipeId}/images/{imageId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| recipeId | path |  | Yes |  |
| imageId | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PATCH*** 

**Summary:** Updates a the image details of a recipe

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/recipes/{recipeId}/images/{imageId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| recipeId | path |  | Yes |  |
| imageId | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/REQUESTS
## ***POST*** 

**Summary:** Creates and commits a Request to be used in the Purchasing Document Workflow.

### HTTP Request 
`***POST*** /api/v{apiVersion}/requests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/REQUESTS/{ID}/COMMIT
## ***PATCH*** 

**Summary:** Commits a Request, this allows the Request to be used in future steps of the Purchasing Document Workflow

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/requests/{id}/Commit` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Request | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/REQUESTS/{ID}
## ***PATCH*** 

**Summary:** Updates an existing Request

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Request | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/SESSIONS
## ***GET*** 

**Summary:** Getting Sessions

### HTTP Request 
`***GET*** /api/v{apiVersion}/sessions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creating new Sessions

### HTTP Request 
`***POST*** /api/v{apiVersion}/sessions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PUT*** 

**Summary:** Updating existing Sessions

### HTTP Request 
`***PUT*** /api/v{apiVersion}/sessions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/SESSIONS/{ID}
## ***GET*** 

**Summary:** Getting Session by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/sessions/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Session Id | Yes |  |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Deleting a Session

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/sessions/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Session Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/SESSIONS/{ID}/SESSIONITEMS
## ***POST*** 

**Summary:** Adding a Session Item to a Session

### HTTP Request 
`***POST*** /api/v{apiVersion}/sessions/{id}/sessionItems` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Session Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/SESSIONS/{ID}/SESSIONITEMS/{SESSIONITEMID}/COUNT
## ***PUT*** 

**Summary:** Updating values of a Session Item

### HTTP Request 
`***PUT*** /api/v{apiVersion}/sessions/{id}/sessionItems/{sessionItemId}/count` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Session Id | Yes |  |
| sessionItemId | path | Session Item Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/STORES
## ***GET*** 

**Summary:** Gets Stores

### HTTP Request 
`***GET*** /api/v{apiVersion}/stores` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/STORES/{ID}
## ***GET*** 

**Summary:** Gets Store by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/stores/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Store Id | Yes |  |
| Expand | query |  | No |  |
| Filter | query |  | No |  |
| OrderBy | query |  | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/STORES/{ID}/INTERFACES/THIRDPARTYCODES
## ***GET*** 

**Summary:** Gets a Store's ThirdPartyCodes

### HTTP Request 
`***GET*** /api/v{apiVersion}/stores/{id}/interfaces/ThirdPartyCodes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Store Id | Yes |  |
| Filter | query | ### Filter Options:  - code  - type | No |  |
| OrderBy | query | ### Order By Options:  - code  - type | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/INTERFACES/THIRDPARTYCODES
## ***GET*** 

**Summary:** Gets all Third Party Codes

### HTTP Request 
`***GET*** /api/v{apiVersion}/interfaces/thirdPartyCodes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - code  - type | No |  |
| OrderBy | query | ### Order By Options:  - code  - type | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creates Third Party Codes

**Description:** ## Standard Request Example

Third Party Codes are configuration options exposed to the Yellow Dog Inventory user that allow for behavior changes for an item or a setting. A common use case is for managing what the tax code might be for a particular item so that the integration is able to associate the proper tax rate on sale of the item.

### POST /thirdPartyCodes

```json
[
	{
		"type": "IntegrationNameTaxGrouping", // This will be displayed in the Interfaces tab under the Accounting/Other section as "Integration Name Tax Grouping"
		"code": "1", // Identifier used by the Integrator to match certain behavior on their side of the integration.
		"description": "local tax" // User friendly description that will be displayed to the user as part of a drop down box titled by the `type`
		"store": {
			"id": "123e4567-e89b-12d3-a456-426655440000" // Id of the store this Code should be active for. If this code should be active for all stores use an id value of "00000000-0000-0000-0000-000000000000"
		}
	}
]
```

## Modifiers Example

If the third party integrator would like to allow enabling of true/false values for allowing Yellow Dog clients to enable item behavior in the integration, we recommend that this be accomplished by the following example.

### POST /thirdPartyCodes

```json
[
	{
		"type": "IntegrationNameIsModifier",
		"code": "true", 
		"description": "Is a Modifier" 
		"store": {
			"id": "123e4567-e89b-12d3-a456-426655440000" 
		}
	},
	{
		"type": "IntegrationNameIsModifier", 
		"code": "false", 
		"description": "Is not a modifier" 
		"store": {
			"id": "123e4567-e89b-12d3-a456-426655440000" 
		}
	}
]
```

### HTTP Request 
`***POST*** /api/v{apiVersion}/interfaces/thirdPartyCodes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| suppressOutput | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Received Request with no values in the body. |
| 201 | Returns the newly created ThirdPartyCodes, if suppressOutput parameter is set to false. |
| 400 | Error has occured. |

## ***PUT*** 

**Summary:** Updates Third Party Codes

### HTTP Request 
`***PUT*** /api/v{apiVersion}/interfaces/thirdPartyCodes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| suppressOutput | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Returns the updated ThirdPartyCodes, if suppressOutput parameter is set to false. |
| 400 | Error has occured. |

## ***DELETE*** 

**Summary:** Bulk delete Third Party Codes

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/interfaces/thirdPartyCodes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| suppressOutput | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/INTERFACES/THIRDPARTYCODES/{ID}
## ***GET*** 

**Summary:** Gets Third Party Code by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/interfaces/thirdPartyCodes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Deleting a Third Party Code

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/interfaces/thirdPartyCodes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Third Party Code Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/THIRDPARTYSESSIONS
## ***GET*** 

**Summary:** Gets all Third Party Sessions

### HTTP Request 
`***GET*** /api/v{apiVersion}/thirdPartySessions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - code  - dateTime | No |  |
| OrderBy | query | ### Order By Options:  - code  - dateTime | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creates Third Party Sessions

### HTTP Request 
`***POST*** /api/v{apiVersion}/thirdPartySessions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| suppressOutput | query |  | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/THIRDPARTYSESSIONS/{ID}
## ***GET*** 

**Summary:** Gets Third Party Session by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/thirdPartySessions/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSACTIONS
## ***GET*** 

**Summary:** Getting all Transactions

### HTTP Request 
`***GET*** /api/v{apiVersion}/transactions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - checkClosed | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creates or Updates Transactions

**Description:** If inserting a new record it is highly recommended that you provide a ThirdPartyId which should correspond
to the ID your system uses to uniquely identify the transaction. If the ThirdPartyId and / or ThirdPartyLineId wasn't
provided the API will auto create one for you.

### HTTP Request 
`***POST*** /api/v{apiVersion}/transactions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| suppressOutput | query | Default: true  If true the api will not respond with transactions created or updated in the response. Errors are still shown if applicable. | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSACTIONS/STORE/{STOREID}
## ***GET*** 

**Summary:** Gets Transactions by Store

### HTTP Request 
`***GET*** /api/v{apiVersion}/transactions/store/{storeId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storeId | path |  | Yes |  |
| Filter | query | ### Filter Options:  - checkClosed | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSACTIONS/{THIRDPARTYID}
## ***GET*** 

**Summary:** Gets Transaction by ThirdPartyId

### HTTP Request 
`***GET*** /api/v{apiVersion}/transactions/{thirdPartyId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| thirdPartyId | path |  | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSFERS/{ID}/ACCEPT
## ***PATCH*** 

**Summary:** Accepts a Transfer

**Description:** Accepting a Transfer is an indication that the Store on the recieving side of the Item movement has
            been recieved at the quantities indicated by the accepting quantity.

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/transfers/{id}/Accept` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSFERS/{ID}/ISSUE
## ***PATCH*** 

**Summary:** Issues a Transfer

**Description:** Issuing a Transfer is an indication that the Store on the sending side of the Item movement 
            has been sent to the Store on the Recieving side.

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/transfers/{id}/Issue` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSFERS
## ***POST*** 

**Summary:** Creates a Transfer

### HTTP Request 
`***POST*** /api/v{apiVersion}/transfers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSFERS/{ID}/LINES
## ***POST*** 

**Summary:** Add Additional lines to an existing Transfer that has not been committed

### HTTP Request 
`***POST*** /api/v{apiVersion}/transfers/{id}/lines` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Delete existing lines from a Transfer

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/transfers/{id}/lines` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PATCH*** 

**Summary:** Updates existing lines of a given Transfer

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/transfers/{id}/lines` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/TRANSFERS/{ID}
## ***PATCH*** 

**Summary:** Updates an existing Transfer

### HTTP Request 
`***PATCH*** /api/v{apiVersion}/transfers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | CommDoc Id of Transfer | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/VENDORS
## ***GET*** 

**Summary:** Getting Vendors

### HTTP Request 
`***GET*** /api/v{apiVersion}/vendors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Filter | query | ### Filter Options:  - code  - description  - url  - collectsTax  - notes  - created  - lastUpdated | No |  |
| OrderBy | query | ### Order By Options:  - code  - created  - lastUpdated | No |  |
| PageNumber | query | - PageNumber Starts at 1 | No |  |
| PageSize | query | - Default page size: 100  - Max page size: 500 | No |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***POST*** 

**Summary:** Creating new Vendors

### HTTP Request 
`***POST*** /api/v{apiVersion}/vendors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***PUT*** 

**Summary:** Updating existing Vendors

### HTTP Request 
`***PUT*** /api/v{apiVersion}/vendors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Bulk delete Vendors

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/vendors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /API/V{APIVERSION}/VENDORS/{ID}
## ***GET*** 

**Summary:** Getting Vendor by Id

### HTTP Request 
`***GET*** /api/v{apiVersion}/vendors/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Vendor Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***DELETE*** 

**Summary:** Deleting a Vendor

### HTTP Request 
`***DELETE*** /api/v{apiVersion}/vendors/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Vendor Id | Yes |  |
| apiVersion | path |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
