## Performance Testing Documentation for Ryanair Website

### • Verify Response Time for 1000 Users

**Objective:** Validate the response time of the Ryanair website under a load of 1000 simultaneous users.

**Steps Taken:**
1. Configured JMeter test plan with a Thread Group set to 1000 users and a ramp-up period.
2. Utilized timers to control the pacing of user requests.
3. Monitored response times using listeners (e.g., Aggregate Report) during test execution.

**Results:**
- Minimum response time recorded: 82 ms
- Average response time observed: 239 ms
- Maximum response time recorded: 501 ms
- Response time remained within acceptable thresholds.



### • Verify Response Time Under Different Load Conditions

**Objective:** Evaluate the response times for the Ryanair website under varied load conditions.

**Procedure:**
1. Created separate Thread Groups for low, normal, moderate, and heavy load scenarios.
2. Defined different user counts and ramp-up periods for each Thread Group.
3. Executed tests for each load scenario and analyzed response times using listeners.

**Observations:**
- Response times:
  - Low Load: Min. response time: 97 ms / Max. response time : 239 ms
  - Normal Load: Min. response time: 91 ms / Max. response time : 259 ms
  - Moderate Load: Min. response time: 75 ms / Max. response time : 246 ms
  - Heavy Load: Min. response time: 87 ms / Max. response time : 267 ms
