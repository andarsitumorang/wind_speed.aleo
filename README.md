# wind_speed.aleo

## Build Guide

To compile this Aleo program, run:
```bash
// Wind speed calculation program.
program wind_speed.aleo {
    // The "WindInfo" struct representing information about wind.
    struct WindInfo {
        // A struct member named "distanceTraveled" with type "field".
        distanceTraveled: field,
        // A struct member named "timeTaken" with type "field".
        timeTaken: field,
    }

    // The "main" function of this Leo program takes a "WindInfo" struct type as input.
    // To pass "windInfo" into the "main" function we
    // 1. Define the "WindInfo" type.
    // 2. Use brackets { } to enclose the struct members.
    // 3. Define each struct member name : value.
    //
    // You can try this transition function by running: 
    // leo run main "{ distanceTraveled: 100field, timeTaken: 10field }"

    transition main(windInfo: WindInfo) -> field {
        // Calculate wind speed based on the formula.
        let windSpeed: field = windInfo.distanceTraveled / windInfo.timeTaken;

        return windSpeed;
    }
}

```

To execute this Aleo program, run:
```bash
leo run main "{ distanceTraveled: 100field, timeTaken: 10field }"
```
