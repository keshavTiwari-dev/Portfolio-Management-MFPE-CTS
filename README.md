# MFPE POD-3
# Prepared by MFPE Pod 3

--Technologies used :-

1. Java 8
2. Spring Data Access JPA
3. Spring Boot
4. Spring Rest
5. Angular
6. Microservices (in built swagger)
7. H2 - in memory
8. JUnit
9. Spring Security
10. Lombok Logging



--Tools used :-

1. Spring Tool Suite
2. Postman
3. Docker




--Modules :-

1. Authorization :- Authorization Microservice is used by all the microservices, to perform the operations that only a 
					logged in user has the privileges to do.
					a. End Points:- 
						1. getToken		POST		/getToken
						2. getUname		GET			/getuname
						3. getId		GET			/getid
					b. Dependency on other microservices :- None
					c. Application.properties :- 
						server.port=8081
						spring.application.name=AUTHORIZATION-SERVICE

2. Calculate net worth :- 
							Calculate Net Worth Microservice performs :-
								- Calculate the current value of share holdings and mutual fund holdings and find out the 
				  				  total current value or net-worth.
								- Sell assets and determine the final net-worth current value or net-worth.
					a. End Points:- 
						1. viewAsset	GET			/viewAsset
						2. sellAsset	POST		/sellAssets
					b. Dependency on other microservices :- DailyMutualFundNAV, DailySharePrice and Authorization
					c. Application.properties :- 
						server.port=8084
						spring.application.name=CALCULATENETWORTH-SERVICE

3. Daily Mutual Fund NAV :- Daily mutual fund NAV Microservice that performs getting NAV (Net Asset Value) of a mutual fund.
					a. End Points:- 
						1. mutualFundName	GET			/mutualFundName
						2. allMutualFund	GET			/allmf
					b. Dependency on other microservices :- CalculateNetworth and Authorization
					c. Application.properties :-
						server.port=8083
						spring.application.name=MUTUALFUNDNAV-SERVICE

4. Daily Share Price :- Daily Share Price Microservice that performs following operation which is getting daily share 
						price of a stock.
					a. End Points:- 
						1. stockName		GET			/stockName
						2. allStock			GET			/allstock
					b. Dependency on other microservices :- CalculateNetworth and Authorization
					c. Application.properties :-
						server.port=8082
						spring.application.name=DAILYSHAREPRICE-SERVICE

5. Swagger :- Swagger is an open source project used to generate the REST API documents for restful web services.
				 It provides a user interface to access our restful web services via the web browser.
					We have implemented swagger in every microservice.
					
					a. Swagger-ui :- localhost:808x/ {where 'x' is specific to a particular microservice's exposed port}




