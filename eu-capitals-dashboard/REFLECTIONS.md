# Reflections

## Before building anything
I care about both, but good weather matters a little more since it's a vacation. I wouldn't ignore CO2, though, if two places had similar weather.

## Acquisition reliability
One request means fewer chances for a timeout or throttling. With 26 separate requests, any one could fail and interrupt the run.

## Provenance
I'd check the factor against a current government source and note the year and assumptions. I'd also explain that this is an estimate, not the emissions for a specific flight.

## Relative vs. absolute
Adding a colder, rainier city doesn't change the other cities' actual temperatures, but it can change their normalized scores. The scores depend on which cities are being compared.

## Predict, then check
I guessed Madrid because it might have a good balance of weather and distance from Paris. I was right: it ranked first (0.754). Lisbon had better weather, but its CO2 score was lower, which pulled down its final score.

## Monitoring
I'd check the "Data last updated" time; if it's old, the workflow may have stopped. I'd add a warning for stale data, since visitors might not know when the timestamp should have changed.

## The unguided step
I changed the origin coordinates and filtering in `scripts/fetch_and_score.py`, then added the origin to the JSON so `docs/index.html` can show it in the title. The best destination isn't absolute: it depends on where the trip starts and on that week's weather.