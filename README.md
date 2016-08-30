"# AssignmentORGSync" 


**ORGANIZATION 1  - LIVE ORG (NEW IMPLEMENTATION)


Requirement 1
  showAccountsFromORG2 -
        - Visualforce Page to show all Accounts from ORG 2.
  OldOrganizationData - 
        - Controller Extension to Visualforce Page.
        - Invocation Layer
        
  IntergationServices
        - Service Layer Class to provide Integration related Service. 
  
  PaginationService
        - Service Layer Class to provide Pagination Service. 
        

Requirement 2 - Sync of similar accounts getting created in ORG 1 and ORG 2.

  AccountTrigger - 
        - Trigger to search and link an ORG 2 Account with any newly created account in ORG 1. 
        - Invocation Layer
        - Logic stored in Level 2 Invocation Layer - AccountTriggerHandler
  
  Recent Update -
    Updated Trigger logic to update all matching record Ids seperated by ':' as a reference when account gets created in ORG 1.
    Updated Trigger logic to work on Update Calls.
    
    
  AccountTriggerHandler
        - Trigger actual Logic 
        - Trigger handler called from Account Object- One Trigger Per Object.


                    
                    
                    
**ORGANIZATION 2 - TARGET ORG (PAST IMPLEMENTATION)

    AccountsResource(/v1/accounts)
        - single REST service exposed from Past Implementation Project.
    
    AccountServices
        - Service Layer class having generic methods related to Accounts Service. 
        
        


