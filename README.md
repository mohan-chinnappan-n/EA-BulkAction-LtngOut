## Einstein Analytics (EA) - Bulk Actions using Lightning Out

In this repo you will find the following:

- Lightning App (EALtngOutApp.app)
- Lightning Component (EALtngOut.cmp)
- Visualforce page (EALtngQuickActionTest.page)

EA bulk Action happens in this sequence:

1. User clicks the custom action - Bulk Action 
2. EA passes query parameter to the Visualforce page (in our case: EALtngQuickActionTest.page)  wired in this custom action (bulk action)
3. EALtngQuickActionTest.page gets the SAQL in url parameter named query 
    - EALtngQuickActionTest.page make POST call to /services/data/v45.0/wave/query with query we got
    - EALtngQuickActionTest.page uses Lightning Out feature to createComponent EALtngOut.cmp via EALtngOutApp.app. 
    - And in this process, the Lighting component gets SAQL query as well as the result of that SAQL query
    - EALtngOut.cmp can now create records or do any bulk action base on the results of the SAQL query returned by the EA


### Demo
!(demo/-Bulk-Actions-LtngOut-1.gif)   
