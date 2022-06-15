# Introduction to Open Street Routing Machine

Author: [Huanfa Chen](https://github.com/huanfachen/)

Last update: 2022/06/15

1. What is OSRM?
   1. An open-source modern C++ routing engine for shortest paths in road networks.
   2. An open-source alternative to Google Map, Gaode Map (Amap), Baidu Map, et al.
   3. The network data is based on OpenStreetMap.
   4. The server can be deployed in an off-line environment without Internet
   5. Supporting driving, bike, foot (but not public transport)
2. Why we need OSRM (given that Google/Gaode/Baidu Maps) are free and fast?
   1. **Not free for large-scale queries**: when you have millions of queries (0.04 USD per query)
   2. **Not secure for high-security projects**: you need to visit Internet; anyone may be forbidden to use these APIs (up to company decisions)
   3. **Not customisable** (if you want to change the road network or simulate the effect of new infrastructures)
3. Why we need road network distance (given that Euclidean distance is an approximately in many geography/transport papers)
   1. Is Euclidean distance always a good approximation? (Multiple mode; infrastructure; et al.)
   2. ![image-20220615154427324](C:\Users\HChen\OneDrive - University College London\Github\OSRM_playground\Image\Example_Euclidean_distance)
   3. The distance or duration is likely to differ across travel modes (driving, cycle, walking)
4. 