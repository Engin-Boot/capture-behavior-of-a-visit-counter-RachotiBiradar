# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given a working hospital
  When for a perticular day of the days in a week intialize a new counter variable
  And when sensor senses a person then increment the counter by one
  And store the value
  And Draw a line graph showing trend
  Then show the trend graph on the screen

Scenario: Alert when seating capacity is full

  Given a working Hospital
  When check the seating capacity 
  And if it is full
  Then show to user message "Seating capacity is full"

