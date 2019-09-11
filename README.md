__Flight Data Metrics Report__

(downloadable pdf available in repository)

* dataset used: https://www.kaggle.com/traceyvanp/airlinefleet

One specific axis I examined the data on that was not mentioned in the dataset specifically but was a point of personal interest for me was Low Cost vs. Traditional carriers. Customers are always trying to save money no matter what service they purchase and there is a growing demand for low cost carriers where customers are willing to sacrifice comfort or amenities for a lower price plane ticket.
I created an extra column in the data called carrier type and used this list (https://brightside.me/wonder-curiosities/a-comprehensive-list-of-all-the-low-cost-airlines-in-the-world-212305/) for reference to mark which airlines are low cost ones and marked the rest as traditional.

Summary of findings
* US-based airlines have the largest fleets; China is not far behind
* Low-cost airlines from Asia have the fastest growth 
*	Low-cost airlines do not try to save money by buying cheaper planes
*	Boeing 747 and Airbus A320 are the most popular planes, the latter even more so with low-cost airlines
*	US-based and China-based airlines do not have the highest fleet longevity
*	Fleet age is not a major deciding factor in ordering new planes

Tools used: dataset analysis was done with SQL and Tableau, as the dataset was fairly small

__Largest Fleets__: 

![largest01](/flightgraphs/largestfleets.jpg)
![largest02](/flightgraphs/largestfleets_sql.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/CurrentFleetSize

* The largest fleets are mostly US-based airlines (American, Delta, United, Southwest) with China not too far behind. This is not too surprising as air travel is very popular in the US for long distance travel. Many business professionals who need to travel for work would prefer a quick flight over a long drive or train ride.
* By the 2015 statistic in this article, the US has the highest amount of air passengers, with China in 2nd place, which matches up with the fleet size data. 
* Also, the largest fleets are mostly comprised of traditional carriers with Southwest and Ryanair being exceptions. Southwest is a particularly popular low cost airline and matches up with anecdotal expectations – friends, family, colleagues, all manner of acquaintances have all enthusiastically recommended Southwest as a favorite choice to fly within the US.


__Fastest Growing Airlines__:

![orders01](/flightgraphs/orders.jpg)
![orders02](/flightgraphs/orders_sql.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/Orders

* Airline growth was determined by looking up the airlines with most planes on order.
(The data used was the Order column as it was more consistent and yielded larger numbers and didn’t have as many missing values as the Future column) 
* From this, it appears that the fastest growing airlines are Lion Air, IndiGo, and AirAsia – all low cost carriers based in Asia, followed by three of the largest US-based airlines (American, Southwest, and Delta). It makes sense that the largest US-based fleets would be on this list as it would continue to grow to fulfill demand, but it’s interesting that Asian airlines are growing at a faster pace – will they ever catch up to the US in fleet size? Might be worth looking into. 


__Current Fleet Size vs. Orders__:

![currentsvsorders](/flightgraphs/currentfleetvsorders.png)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/CurrentFleetvs_Orders

* The blue cluster of dots on the upper left are Lion Air, IndiGo, and AirAsia – the rapidly growing low-cost airlines from Asia. They have all ordered far more planes than their current fleet size!
* On the other hand, the large US-based airlines have ordered a substantial number of planes to grow their fleet (roughly ~1/3 the existing fleet size) but still have a large enough fleet they can use what they already have to meet the demands of customers.
* The bubble size represents average unit cost (in $M) of planes in the fleet. Do low cost airlines tend to order cheaper planes than traditional ones in the interest of profit? Well…


__Most Expensive Planes__: 

![mostexpensive](/flightgraphs/mostexpensive.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/MostExpensivePlanes

* Here’s a detailed look at whether the most expensive planes were primarily bought by traditional airlines (or avoided by low cost airlines) and the answer is no, not really! The top 7 results were popular with low cost airlines as well. One probable explanation is that air travel has to meet rigorous safety standards so quality and reliability is far more important than trying to keep costs low for profit reasons.


__Most Popular Planes__:

* Most Currently Used: 
![mostcurrentlyused](/flightgraphs/mostcurrentlyused.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/MostCurrentlyUsedPlanes

Out of the most currently used planes, the Boeing 737 and Airbus A320 are popular with both low cost and traditional airlines, whereas the rest seem to be mostly favored by traditional airlines.
 
* Most Ordered: 
![mostordered](/flightgraphs/mostordered.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/MostOrderedPlanes

In fact, the Airbus A320 is so popular with low cost airlines that out of the most ordered planes, the majority of those orders are placed by low cost airlines. The Boeing 737 continues to be a favorite go-to for both airline types. 

* Most Retired: 
![mostretired](/flightgraphs/mostretired.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/MostRetiredPlanes

I was curious about trends in retired planes and noticed that McDonnell Douglas showed up for half the results in the top 10 so I did some extra research and turns out Boeing bought and merged with McDonnell Douglas in 1997, and several McDonnell Douglas planes had unfavorable reputations in the past due to a high frequency of accidents and were eventually permanently retired – all of which makes sense with the data. As for the Boeing 737 being the top result for retired plane – it just simply means that it’s a very commonly used plane. Seeing how the numbers are high for both current fleet and orders, the high retired number does not actually indicate decline.


__Oldest Fleets__: 

![oldest](/flightgraphs/oldest.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/OldestFleets

* None of the oldest fleets (by average age of current planes in the fleet) were listed among the largest and only one of them (Air Transport International) is US-based and none of them are Chinese airlines. It’s worth pointing that out as mentioned before, because US and China have the largest amount of air passengers, their planes will get the most frequent use and will likely not last as long/will have to be replaced sooner for safety reasons.    

* Average Age of Fleet vs. Orders

![agevsorders](/flightgraphs/agevsorders.jpg)
https://public.tableau.com/profile/sonia.yang#!/vizhome/FlightData_15681918430980/FleetAverageAgevs_Orders

As suspected, there are no particularly distinct trends between fleet age and orders placed, which means other factors (such as growing customer demand) influence plane orders more.

