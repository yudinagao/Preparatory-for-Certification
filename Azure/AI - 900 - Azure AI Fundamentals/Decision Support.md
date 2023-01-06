# Decision Support

## anomaly Detector
- determine whether values in a series are within expected parameters
- act of identifying events or observations, thar differs in a significant way from the rest of the data
- prompts troubleshooting
    - avoiding revenue loss
    - maintain brand reputation

Azure anomaly detection
- cloud based service
- monitor time series data
- can use REST API to integrate Anomaly Detector    
    - the service use the one parameter strategy
        -   the mains parameter is sensitivity - 1 to 99
        - can detect in historical time series or in real time data

- Boundary
    - lower and upper boundarys
        - expectedValue
        - upperMargin
        - lowerMargin
        - marginScale]
    upperBoundary = expectedValue + (100 - marginScale) * upperMargin

- Data Format
    - JSON
        - granularity
        - timestamp
        - value
    - 8640 data points in the same JSON
        - can be reduced to reduce latency

- Data consistency
    - sampling occurs evety few minutes and has less than 10% of the expected of points missing
    - more than 10% - there are option to "fill"
        - linear interpolation
    
Batch Detection
    - entire dataset at one time
    - best used when
        - flat trend time series data with ocasional spikes or dips
        - seasonal time series data with occasional anomalys
            - seasonality is considered to be a pattern in your data and occurs at regular intervals

Real Time detection
    - Compares the previously seen data points to the last data point to determine if is an anomaly
    

