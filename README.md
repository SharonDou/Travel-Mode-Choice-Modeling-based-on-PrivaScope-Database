# Travel-Mode-Choice-Modeling
Connected & Automated Vehicles (CAV) technology has reached the home stretch of commercialization. For the sake of making the product more economic, many people believe that rides will be combined and electrified. MCity, as a leader in CAV testing and deployment, has decided to operate the first automated shuttle line on the campus of the University of Michigan in 2017. To enhance the performance of this new mobility system and ensure its compatibility with existed facilities, we will assist the team by modeling the traveling pattern of U-M community members. The main and unique resource we will leverage on is the PrivaScope database that tracks all WiFi devices on campus. We hope to develop a data-driven algorithm for vehicle routing and scheduling use. At the end of day, it should be able to allocate automated shuttles efficiently to meet dynamic demand for traveling between campus.

Database:
PrivaScope:
Assuming that mobile devices (especially cellphone) represents the realtime movements of people (U- M faculty members, staff and students) on campus. We can estimate the current travel mode choice based on locations of connected WiFi access point, i.e. hotspot. We can construct paths from point- to-point geometric connections.

Three databases are used in this project (only introduce columns we may use):
1. MCommunity database: information about a U-M member’s identity i.e. name and position (faculty member, staff or student) and unique id. One’s unique id is the same as his or her WiFi login name.
2. WiFi connection database: include device information (series number, etc.), time (in second) and connected hotspot id.
3. WiFi hotspot id map: each hotspot id has its geographic location, which is labeled by the centroid of a nearest building on campus map.

Task Description:
1. Build a database of device users’ paths.
Path is a series of connected geometric locations on a map.
A.
B.
Create a table that links devices (from device series number) to their owners (MCommunity data).
Construct O-D paths with data structure of: User ID:
Trip:
Start point – trip starting time - hotspot id – location on map – mobility mode Second point – time - hotspot id – location on map – mobility mode
...
End point – trip ending time - hotspot id – location on map – mobility mode
The challenge is estimating the mobility mode. We can start by testing human-made rules. For example, the average speed moving from one spot to next spot, access to nearest public transport or parking, etc. More advanced machine learning technique for classification can also be applied when rules are not sufficient.
The accuracy of classification is hard to test either. It may only be compared with manual classification, which is also subjective.
2. Combine trips by travel mode to check the feasibility of automated shuttle service on campus, as well as estimate the occupancy of current proposed route.
3. Optimize the routing and scheduling of shuttle service between NCRC and North Campus (2 buses, multiple stops from existed stops).
4. Propose for future services.
