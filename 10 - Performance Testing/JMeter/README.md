## Performance Testing Documentation for Ryanair Website

### 1. Verify Response Time for 1000 Users

**Objective:** Validate the response time of the Ryanair website under a load of 1000 simultaneous users.

**Steps Taken:**
1. Configured JMeter test plan with a Thread Group set to 1000 users and a ramp-up period.
2. Utilized timers to control the pacing of user requests.
3. Monitored response times using listeners (e.g., Aggregate Report) during test execution.

**Results:**
- Average response time observed: 239 ms
- Maximum response time recorded: 633 ms
- Response time remained within acceptable thresholds.

### 2. Check Application Capacity Before Crashing

**Objective:** Assess the application's capacity by gradually increasing the user load until errors or performance degradation occur.

**Approach:**
1. Set up Thread Groups representing different load scenarios (low, normal, moderate, heavy).
2. Increased user counts gradually while monitoring performance metrics and system resources using JMeter listeners and plugins.
3. Identified the threshold where the application started exhibiting issues.

**Findings:**
- Low Load (50 users): Response times within acceptable range.
- Normal Load (100 users): Minor increase in response times observed.
- Moderate Load (200 users): Increased response times and error rates noticed.
- Heavy Load (500 users): Application experienced performance degradation and increased errors.

### 3. Check Database Execution Time for 500 Records

**Objective:** Measure the execution time for database operations involving 500 records.

**Execution:**
1. Configured JMeter's JDBC Sampler to perform read/write operations on the database.
2. Parameterized JDBC requests to handle 500 records.
3. Monitored database execution time and response times using appropriate listeners.

**Outcome:**
- Average database execution time for 500 records: [Insert Execution Time]
- System resources during database operations remained stable.

### 4. Verify Response Time Under Different Load Conditions

**Objective:** Evaluate the response times for the Ryanair website under varied load conditions.

**Procedure:**
1. Created separate Thread Groups for low, normal, moderate, and heavy load scenarios.
2. Defined different user counts and ramp-up periods for each Thread Group.
3. Executed tests for each load scenario and analyzed response times using listeners.

**Observations:**
- Response times:
  - Low Load: [Insert Response Time]
  - Normal Load: [Insert Response Time]
  - Moderate Load: [Insert Response Time]
  - Heavy Load: [Insert Response Time]
