# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given a working Hospital and is open on both working days and Holidays
  When initialize a counter from "0"
  And when sensor senses a person increase the counter by "1"
  Then show the aggregated result on the Report.

Scenario: Compute parking slots to reserve for visiting specialists

  Given a working Hospital and is open on both working days and Holidays
  When I take number of vehicles present in the same day last week 
  And If there is deficiency in parking slots then I increse the parking slots
  Else leave as it is
  Then the number of Parking slots Reserved is added to the result.
