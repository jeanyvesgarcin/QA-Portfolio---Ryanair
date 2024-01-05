## Performance Testing Documentation for Ryanair Website

_Reports written with the help of Claude AI_


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

**Analysis:**
The average response time of 239 ms is well within the acceptable threshold of 1000 ms for an e-commerce website. The maximum response time of 501 ms for some requests is higher than desired but still reasonable given the load. The overall results indicate the Ryanair website is performing well under a load of 1000 simultaneous users.

**Further Investigation:**
To fully validate performance, the test should be executed multiple times to check for consistency of results. Additional tests should also be run with higher user loads (e.g. 2000, 3000 users) to determine the breaking point where response times start to degrade significantly.

Transaction response times should be analyzed to identify any specific bottlenecks by page or functionality on the site. Load testing should also be conducted from different geographic regions to account for network latency.

**Next Steps:**

1. Execute load test 3 more times with 1000 users to validate consistency
2. Increase load in increments of 1000 users and identify response time degradation tipping point
3. Analyze transaction performance to find pages/functions with high response times
4. Execute tests from different regions and compare geographic response times



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

**Analysis:**
The Ryanair website maintained good response times under low to moderate load conditions, with all response times well under the 1000 ms threshold. At heavy load, response times remained reasonable though latency increased slightly. This indicates that the website infrastructure can scale effectively. Specific transactions should be analyzed to identify potential bottlenecks.

**Further Investigation:**
Tests should be executed with greater user loads (5000+) to find the breaking point. Percentile response times (90th, 95th) should be analyzed to account for outliers. Transactions causing longer response times need to be optimized. Load generation from different regions also needs to be validated.

**Next Steps:**

1. Execute load tests with higher user volumes in increments
2. Analyze percentile response times under different loads
3. Profile transactions with longer response times for optimization
4. Test response times from multiple geographic regions
