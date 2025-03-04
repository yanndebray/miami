Yann:
create a dataset for the temperature forecast over 3 days, sampling every 3 hours, store it as a table

Copilot:
To create a dataset for temperature forecasts over 3 days, sampling every 3 hours, and store it as a table in MATLAB, you can use the following code:

```matlab
% Define the time range
startTime = datetime('now'); % Current time
endTime = startTime + days(3); % 3 days later
timeVector = startTime:hours(3):endTime; % Sampling every 3 hours

% Generate random temperature data (for example purposes)
temperatureData = randi([15, 30], length(timeVector), 1); % Random temperatures between 15 and 30 degrees

% Create the table
temperatureForecast = table(timeVector', temperatureData, ...
    'VariableNames', {'Time', 'Temperature'});

% Display the table
disp(temperatureForecast);
```

### Explanation:
- `datetime('now')` gets the current date and time.
- `startTime:hours(3):endTime` creates a vector of times from the start time to the end time, sampled every 3 hours.
- `randi([15, 30], length(timeVector), 1)` generates random temperature values between 15 and 30 degrees Celsius.
- `table` constructs a table with the specified variable names. 

This code will create a table with two columns: `Time` and `Temperature`, containing the forecasted temperatures for the next three days.

