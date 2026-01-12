SPRING BOOT FOR API
-------------------

OBJECTIVES COVERED BY THE PROJECT 
---------------------------------

1)IT EXECUTED RESPONSES AND REQUESTS FROM JSON                
2)OPERATED IN CORRESPONDENCE TO THE CREATE/READ
/UPDATE/DELETE OPERATIONS                       
3)IMPLETED AN H2 DATABASE WITH SPRING DATA JPA AND SWAGGER UI FOR DOCUMENTATION 
ALONG SIDE WITH POSTMAN    
4)DIRECTED EXCEPTION HANDLING WITH PROPER RESPONDINGS 

DIRECTORIES INVOLVED FOR THE PROJECT
------------------------------------

1)LOMBOK

2)SPRING DATA JPA

3)SPRING WEB 

4)H2 DATABASE

5)SPRING BOOT

<img width="300" height="225" alt="Screenshot 2026-01-12 at 14 10 07" src="https://github.com/user-attachments/assets/fee0c060-036a-4e37-ae90-b7abea621d15" /> <img width="300" height="300" alt="Screenshot 2026-01-12 at 15 00 56" src="https://github.com/user-attachments/assets/c77b4057-0742-41a5-b057-a38a698ffe11" />

THE PROJECT STRUCTURE  & EXECUTED PROJECT                 

<img width="250" height="250" alt="Swagger post" src="https://github.com/user-attachments/assets/a9ceb367-2277-4c10-8524-61f205dfe3b3" /> <img width="250" height="250" alt="postman post" src="https://github.com/user-attachments/assets/62262a81-b4d0-4542-990a-4e9470320c66" /><img width="250" height="250" alt="Screenshot 2026-01-12 at 14 28 52" src="https://github.com/user-attachments/assets/db539204-0b01-4a7c-9e0a-130108a03877" />


ABOVE ARE TWO REPRESENTATION OF THE CREATE OPERATION IN POSTMAN AND SWAGGER BOTH INDICATED 
A STATUS OF 201 OK MEANING THAT IT HAS BEEN CREATED AND IMPLENTED AT THE H2 DATABASE ... 
THE TWO "FIRST PRODUCTS ARE AN INDICATION THAT A JSON WAS SENT FROM BOTH SWAGGER AND POSTMAN
INDICATING THAT THEY ARE BOTH FULLY FUNCTIONAL 


HOW THE PROGRAM GOES ABOUT THE POST OPERATION :
-----------------------------------------------

1)THE USER(US) SENDS A JSON FORMAT VIA POSTMAN OR SWAGGER 

2)THE @RequestBody WILL THEN MAP THE JSON BODY FORMAT TO THE ProductRequest

3)THE ProductController THEN CALLS OUT THE ProductService ASPECT

4)THE ProductService WILL THEN PROCESS THE LOGIC

5)WITH A CLASH OF DATA FORMATS THE ProductMapper CONVERTS OBJECTS TO ALLOW THE 
ProductRepository TO SAVE IT AT THE H2 DATABASE

6)RESPONSE IS THEN SENT WITH A HTTP 201 STATUS CREATED 


POSTING JSONs TO THE H2 DATABASE TO MATCH WITH THE DOCUMENTED ONE BY THE PROFESSOR AS WELL AS SHOWING FULL FUNCTIONALITY OF THE OTHER OPERATIONS
------------------------------------------------------------------------------------------------------------------------------------------------

<img width="150" height="150" alt="first" src="https://github.com/user-attachments/assets/ce3c47e6-9290-4446-b5ad-637eb7fa177e" /><img width="150" height="150" alt="second" src="https://github.com/user-attachments/assets/22eda70e-dd86-4611-9c7e-8d924eb65fb3" /><img width="150" height="150" alt="third" src="https://github.com/user-attachments/assets/14bd9743-931a-45b1-b454-2842cc8be902" /><img width="150" height="150" alt="forth" src="https://github.com/user-attachments/assets/587920a3-8a71-4e83-8e5b-a0d411cc8218" /><img width="150" height="150" alt="fifth" src="https://github.com/user-attachments/assets/03320e41-4fd5-41af-b631-2be536388673" />

USING POSTMAN FOR THE POSTING OF THE JSONs

<img width="400" height="400" alt="ALL ITEMS" src="https://github.com/user-attachments/assets/630259af-3c3b-444f-b858-b6c4a58bdf65" /> <img width="400" height="400" alt="GET NONE EXISTING ID" src="https://github.com/user-attachments/assets/b1b0f22e-e5f2-480c-a401-dc99ccd4660b" />

ABOVE ARE TWO INDICATIONS OF THE GET(READ) OPERATIONS 
FIRST CASE IS RETRIEVING ALL PRODUCTS IN WHICH IF INTENDED WANTED TO COLLECT JUST ONE WE WILL 
WOULD JUST SPECIFY THE ID ON THE products/{id section here}
SECOND CASE IS RETRIEVING A NONE EXISTING PRODUCT IN WHICH WE WANTED TO OBTAIN A PREVIOUSLY DELETED PRODUCT ID FOUR AND THE CUSTOM EXCEPTION 
AS INDICATED IS PRODUCTNOTFOUNDEXCEPTION WHICH IS SHOWING A MESSGAE RESPONSE OF THE: "Product with 4 not found " 

<img width="400" height="400" alt="update " src="https://github.com/user-attachments/assets/a7276755-bb88-48f4-bf24-bb13025d79a4" /><img width="400" height="400" alt="update2" src="https://github.com/user-attachments/assets/2422a0fe-6ce0-45c7-953a-e921b26f8346" />

UPDATING THE H2 DATABASE THE ID NUMBER 2 FROM TWOBEFOREUPDATE TO TWOAFTERUPDATE  USING SWAGGER

<img width="300" height="300" alt="Delete" src="https://github.com/user-attachments/assets/2e5e4e97-28dd-4473-b7c8-21d768d30cc0" /><img width="300" height="300" alt="Delete 2" src="https://github.com/user-attachments/assets/136997e8-2d14-4289-9e2e-b9f618207475" /><img width="300" height="300" alt="delete3" src="https://github.com/user-attachments/assets/cb57414c-d3a0-451d-b040-401d798de84f" />

ABOVE ARE THREE INDICATIONS OF THE DELETION OPERATION
THE FIRST IS A SUCCESSFULL ATTEMPT IN DELETE THE ID 4 PRODUCT
THE SECOND IS A CLEAR INDICATION OF THE ABSENCE OF ID 4 PRODUCT IN OUR H2 DATABASE 
THE THIRD IS AN ATTEMPT TO DELETE A NONE EXISITING ENTITY OF WHICH SINCE 4 IS NO LONGER AN ENTITY THE RESULT
OF THISE WOULD BE A PRODUCTNOTFOUNDEXCEPTION FOLLOWING A CORRESPONDING MESSAGE RESPONSE OF THE: "Product with 4 not found " 

HOW THE PRODUCTSERVICE CLASS DOES NOT THROW ERRORS IF IT USES METHODS NOT IMPLEMENTED IN THE PRODUCTREPOSITORY CLASS:
---------------------------------------------------------------------------------------------------------------------

THE ProductRepository EXTENDS JpaRepository ,AND THE SpringData JPA Dependency AUTOMATICALLY PROVIDES IMPLEMANTATIONS OF THE METHODS
SUCH AS SAVE,FINDBYID,FINDALL AND DELETEBYID







