# Freefall-Drift-Calculator
Skydiving freefall drift calculator

This is my first Javascript app I'm developing while learning. Below are some notes for any onlookers who may be interested in the 
calculations or why I elected to do things a certain way.

The tool uses tried and true estimations to determine the ideal "spot" or window of opportunity a skydiver must identify before exiting the aircraft on a routine jump in order for them to make it to their ideal landing zone or "LZ." A skydiver or instructor can use these calculations to identify on a map what he/she should be looking at when they are in the plane to determine if they are within that sweet spot or not.

Further, this tool will identify the direction the skydiver will drift while in freefall and as a consequence reveal to the jumper their ideal spot for deploying their parachute. Additional calculations can be made to plan a canopy descent and this feature may be added over time.

Assumptions:

This calculation is made by taking a few measured assumptions which are typical in a standard belly-to-earth skydive. More advanced jumps may require additional calculations, but this will provide a great starting point of reference.

We are assuming an average of 60 seconds of freefall
We are assuming the jump will be made from 13,500ft AGL or above 12,0000ft
We are assuming the winds aloft forecast is accurate

Calculations:

Freefall Drift Direction:

Using the posted winds aloft data for your area the app will average out the directions for all altitudes you will "fall through." For example, a jump from 13,500ft AGL will average the wind direction for 3k', 6k', 9k', and 12k' resulting in the average wind direction expressed in compass degrees.

Ex: Winds Aloft Report
3k - 270
6k - 300
9k - 310
12k - 240

270 + 300 + 310 + 240 / 4 = 280degrees = West North-West

Freefall Drift Distance:

Again using the winds aloft data for your area the app will calculate the average wind speed for the altitudes you will "fall through." The app also takes into account "body throw," or the standard amount of distance your body travels with the plane before you are subject to freefall drift. It then converts the speed from knots (kts) to miles/hour (mph) and adjusts for the standard time in freefall (60 seconds). This calculation results in a decimal integer representing the amount of miles you will drift while in freefall.

Ex: Winds Aloft Report
3k - 40kts
6k - 45kts
9k - 30kts
12k- 50kts

40 + 45 + 30 + 50 = 165kts / 4 = 41.25kts * 1.15 (kts to mph conversion) = 47.4375mph / 60sec = 0.79mi - .2 (avg body throw) = .59mi

After a user has made these calculations they can view a map of their drop zone and be equipped with the knowledge of which direction the plane should be flying on jump run, where the plane should be when the exit light goes on, how far and what direction they will drift while making their jump and make a judgement on the optimal area to deploy their parachute in order to land at their intended LZ.
