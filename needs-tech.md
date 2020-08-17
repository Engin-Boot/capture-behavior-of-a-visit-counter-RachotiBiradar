# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given the server was Running before and has saved the data of previous days
  When I Restart the server all the data stored should be Retrieved
  Then the server is kept open to continue the process

Scenario: Reconcile counts if the sensor is offline for a while

  Given sensor was offline for a while and now Running
  When I Restart the sensor the sensor has to start the count 
  Then the sensor starts sensing and keeps track of number of people entering.
