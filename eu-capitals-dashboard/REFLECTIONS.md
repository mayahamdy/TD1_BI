# Reflections

## Before building anything
I would give weather and CO2 similar importance, with a slight preference for pleasant weather because this is a vacation. I would not ignore either: a much lower-emission option could outweigh a modest weather advantage.

## Acquisition reliability
A batch request needs only one network connection, so there are fewer opportunities for TLS setup, timeouts, throttling, or transient failures. With separate requests, any one of 26 connections can fail and interrupt an otherwise successful run; batching reduces that failure surface as well as the runtime.

## Provenance
Before publishing this for real, I would verify the factor against a current, authoritative source such as the latest government greenhouse-gas conversion factors, record the exact source, year, flight assumptions, and whether the value is per passenger-kilometre, then update the constant and displayed provenance. I would also make clear that a distance-based estimate is not a route-specific flight emissions calculation.

## Relative vs. absolute
Adding a colder, rainier capital does not change the measured temperature of any existing capital, but it can change their normalized scores because the minimum or maximum used to scale the list may change. That means a raw measurement describes an observed quantity, while a KPI built from relative normalization depends on the comparison group and scoring choices.

## Predict, then check
My prediction is Madrid. I expect it to have relatively favorable weather while being closer to Paris, and therefore lower-emission, than warmer southern destinations such as Lisbon or Athens; that could make it a strong compromise under the equal weather-and-CO2 weighting.
The prediction matched the live run: Madrid ranked first with a final score of 0.754 (weather 0.803, CO2 0.706). Lisbon had a higher weather score (0.898) but a lower CO2 score (0.557), so the equal weighting favored Madrid's compromise.

## Monitoring
The visible "Data last updated" timestamp is the first signal I would check: if it becomes unexpectedly old, the scheduled pipeline may have stopped or failed. A timestamp alone is not enough because visitors may not know when it should change, so I would also show a freshness warning after a defined age and link to the latest workflow status.