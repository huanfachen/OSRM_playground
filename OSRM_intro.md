# Introduction to Open Street Routing Machine

Author: [Huanfa Chen](https://github.com/huanfachen/)

Last update: 2022/06/15

1. What is OSRM?
   1. An open-source modern C++ routing engine for shortest paths in road networks.
   2. An open-source alternative to Google Map, Gaode Map (Amap), Baidu Map, et al.
   3. The network data is based on OpenStreetMap.
   4. The server can be deployed in an off-line environment without Internet
   5. Supporting driving, bike, foot (but not public transport)
2. Why we need OSRM (given that Google/Gaode/Baidu Maps are free and fast)?
   1. **Not free for large-scale queries**: when you have millions of queries (0.04 USD per query)
   2. **Not secure for high-security projects**: you need to visit Internet; anyone may be forbidden to use these APIs (up to company decisions)
   3. **Not customisable** (if you want to change the road network or simulate the effect of new infrastructures)
3. Why we need road network distance (many geography/transport papers using Euclidean distance)
   1. Is Euclidean distance always a good approximation? (Multiple mode; infrastructure; et al.)
   2. ![image-20220615154427324](C:\Users\HChen\OneDrive - University College London\Github\OSRM_playground\Image\Example_Euclidean_distance.jpg)
   3. The distance or duration is likely to differ across travel modes (driving, cycle, walking)
4. Key functions of OSRM
   1. Nearest - Snaps coordinates to the street network and returns the nearest matches
   2. Route - Finds the fastest route between coordinates
   3. Table - Computes the duration or distances of the fastest route between all pairs of supplied coordinates
   4. Match - Snaps noisy GPS traces to the road network in the most plausible way
   5. Trip - Solves the Traveling Salesman Problem using a greedy heuristic
   6. Tile - Generates Mapbox Vector Tiles with internal routing metadata
5. What you need to deploy and use OSRM
   1. OSRM backend: based on Docker (cross platform, but Linux is recommended over Windows)
   2. OSRM frontend: I haven't used it before
6. Which companies are using OSRM?
   1. Uber: In Uber’s early days, we used a combination of routing engines (including [OSRM](http://project-osrm.org/)) to produce an ETA. (We didn’t have in-app navigation at this point, so we only used it for the ETA and map matching to display vehicle locations.)
   2. 

