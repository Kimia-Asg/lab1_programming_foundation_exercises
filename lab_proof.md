# HomeGuard Security System — Lab Proof

**Author:** Kimia Asgari

**Program file:** homeguard_system.ipynb

**How to run:** Open the notebook in Jupyter (or VS Code) and click "Run All".
Then call run_simulation("AWAY", 3) or run_simulation("HOME", 3).

## How it works
This program uses a Sensor class to represent each home sensor, with methods 
to generate a random reading and check it against thresholds using if/else 
logic. The main loop runs several rounds, reads every sensor, and prints a 
timestamped alert whenever a reading is abnormal for the current mode.

## Sample output

=== HomeGuard Security System ===
Mode: AWAY

Time: 00:39:03
[READING] Living Room motion: 0
[READING] Front Door door: 1
[ALERT!] 🚨 HIGH: SECURITY: Front Door opened while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Kitchen temperature: 66
[READING] Bedroom smoke: 1
[ALERT!] 🚨 HIGH: SAFETY: Smoke detected — fire risk!
[LOG] [00:39:03] Sending notification to homeowner...

Time: 00:39:03
[READING] Living Room motion: 1
[ALERT!] 🚨 HIGH: SECURITY: Motion detected while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Front Door door: 1
[ALERT!] 🚨 HIGH: SECURITY: Front Door opened while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Kitchen temperature: 94
[READING] Bedroom smoke: 1
[ALERT!] 🚨 HIGH: SAFETY: Smoke detected — fire risk!
[LOG] [00:39:03] Sending notification to homeowner...

## Edge case I handled
When a temperature sensor reads below 35°F, the program returns the SAFETY 
alert instead of the milder COMFORT alert, because the safety check runs 
first. A dangerous condition should always take priority over comfort.

# HomeGuard Security System — Lab Proof

**Author:** Kimia Asgari

**Program file:** homeguard_system.ipynb

**How to run:** Open the notebook in Jupyter (or VS Code) and click "Run All".
Then call run_simulation("AWAY", 3) or run_simulation("HOME", 3).

## How it works
This program uses a Sensor class to represent each home sensor, with methods 
to generate a random reading and check it against thresholds using if/else 
logic. The main loop runs several rounds, reads every sensor, and prints a 
timestamped alert whenever a reading is abnormal for the current mode.

## Sample output

=== HomeGuard Security System ===
Mode: AWAY

Time: 00:39:03
[READING] Living Room motion: 0
[READING] Front Door door: 1
[ALERT!] 🚨 HIGH: SECURITY: Front Door opened while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Kitchen temperature: 66
[READING] Bedroom smoke: 1
[ALERT!] 🚨 HIGH: SAFETY: Smoke detected — fire risk!
[LOG] [00:39:03] Sending notification to homeowner...

Time: 00:39:03
[READING] Living Room motion: 1
[ALERT!] 🚨 HIGH: SECURITY: Motion detected while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Front Door door: 1
[ALERT!] 🚨 HIGH: SECURITY: Front Door opened while in AWAY mode!
[LOG] [00:39:03] Sending notification to homeowner...
[READING] Kitchen temperature: 94
[READING] Bedroom smoke: 1
[ALERT!] 🚨 HIGH: SAFETY: Smoke detected — fire risk!
[LOG] [00:39:03] Sending notification to homeowner...

## Edge case I handled
When a temperature sensor reads below 35°F, the program returns the SAFETY 
alert instead of the milder COMFORT alert, because the safety check runs 
first. A dangerous condition should always take priority over comfort.