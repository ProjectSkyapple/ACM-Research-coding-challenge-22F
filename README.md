# Fall 2022 ACM Research Coding Challenge Solution: Mean Car Reliability Rating per State

## The Problem

Assuming that the Kaggle dataset CarsForSale can be a representative sample of all cars available for sale in the United States, I wanted to answer the question: "Which U.S. states generally sold more reliable cars than others?".

## Approach

To successfully determine the answer to this question, I had to write a Python program that does the following:

1. Converts the raw data file "cars_raw.csv" from the CarsForSale dataset into something more usable by Python—a list of dictionaries.

2. Uses the raw data to create a list (sorted by the alphabetical order of the states) of each car's state where the car is sold and the car's reliability rating.

3. Uses this sorted list to generate another list of 50 lists or tuples each containing a state and a set of all reliability ratings from all cars sold from that state.

4. Calculates the average car reliability rating of each state and appends it to each list or tuple described in step 3.

5. Prints two lists—one in alphabetical order and another by ranked order (from highest to lowest mean rating)—containing each state's mean car reliability rating and the number of ratings each state received.

6. Generates and outputs a graphical representation of these lists ("ACRRPS_graph.png").

The code utilizes the Pandas, Seaborn, and Python's built-in libraries such as the CSV library.

The code ("somethingcool.ipynb") is located in the root of this repo.

## Conclusion

The following are code outputs:

```
  AVERAGE CAR RELIABILITY RATING PER STATE
  Calculated based on data from Cars.com
  Ratings are based on a traditional scale from 1.0 to 5.0.

  Sorted by A-Z -------
  - AK: 4.8 (1 rating)
  - AL: 4.774999999999999 (72 ratings)
  - AR: 4.670731707317077 (41 ratings)
  - AZ: 4.675581395348846 (344 ratings)
  - CA: 4.580988023952118 (668 ratings)
  - CO: 4.641772151898725 (158 ratings)
  - CT: 4.735353535353532 (99 ratings)
  - DE: 4.661538461538461 (13 ratings)
  - FL: 4.682657657657712 (888 ratings)
  - GA: 4.604336734693891 (392 ratings)
  - HI: 4.7562500000000005 (16 ratings)
  - IA: 4.705714285714287 (35 ratings)
  - ID: 4.753571428571429 (28 ratings)
  - IL: 4.650421585160212 (593 ratings)
  - IN: 4.6644808743169275 (183 ratings)
  - KS: 4.706172839506173 (81 ratings)
  - KY: 4.696202531645571 (79 ratings)
  - LA: 4.694117647058827 (51 ratings)
  - MA: 4.741562500000003 (320 ratings)
  - MD: 4.714241486068119 (323 ratings)
  - ME: 4.825 (8 ratings)
  - MI: 4.6805970149253735 (268 ratings)
  - MN: 4.728947368421037 (228 ratings)
  - MO: 4.708823529411754 (170 ratings)
  - MS: 4.543478260869566 (23 ratings)
  - MT: 4.75 (4 ratings)
  - NC: 4.68034934497815 (229 ratings)
  - ND: 4.728571428571428 (14 ratings)
  - NE: 4.802702702702704 (37 ratings)
  - NH: 4.665000000000001 (80 ratings)
  - NJ: 4.642136498516329 (337 ratings)
  - NM: 4.720000000000001 (5 ratings)
  - NV: 4.6935483870967705 (93 ratings)
  - NY: 4.66727272727274 (440 ratings)
  - OH: 4.701823708206691 (329 ratings)
  - OK: 4.728888888888892 (45 ratings)
  - OR: 4.648648648648649 (37 ratings)
  - PA: 4.711702127659578 (282 ratings)
  - RI: 4.731428571428572 (35 ratings)
  - SC: 4.7331288343558215 (163 ratings)
  - SD: 4.78695652173913 (23 ratings)
  - TN: 4.739156626506017 (166 ratings)
  - TX: 4.700653061224475 (1225 ratings)
  - UT: 4.773972602739726 (73 ratings)
  - VA: 4.710000000000008 (340 ratings)
  - VT: 4.685714285714285 (7 ratings)
  - WA: 4.701818181818172 (165 ratings)
  - WI: 4.69055118110236 (127 ratings)
  - WV: 4.746153846153845 (13 ratings)
  - WY: 4.733333333333333 (3 ratings)

  Sorted by Highest to Lowest -------
  1. ME: 4.825 (8 ratings)
  2. NE: 4.802702702702704 (37 ratings)
  3. AK: 4.8 (1 rating)
  4. SD: 4.78695652173913 (23 ratings)
  5. AL: 4.774999999999999 (72 ratings)
  6. UT: 4.773972602739726 (73 ratings)
  7. HI: 4.7562500000000005 (16 ratings)
  8. ID: 4.753571428571429 (28 ratings)
  9. MT: 4.75 (4 ratings)
  10. WV: 4.746153846153845 (13 ratings)
  11. MA: 4.741562500000003 (320 ratings)
  12. TN: 4.739156626506017 (166 ratings)
  13. CT: 4.735353535353532 (99 ratings)
  14. WY: 4.733333333333333 (3 ratings)
  15. SC: 4.7331288343558215 (163 ratings)
  16. RI: 4.731428571428572 (35 ratings)
  17. MN: 4.728947368421037 (228 ratings)
  18. OK: 4.728888888888892 (45 ratings)
  19. ND: 4.728571428571428 (14 ratings)
  20. NM: 4.720000000000001 (5 ratings)
  21. MD: 4.714241486068119 (323 ratings)
  22. PA: 4.711702127659578 (282 ratings)
  23. VA: 4.710000000000008 (340 ratings)
  24. MO: 4.708823529411754 (170 ratings)
  25. KS: 4.706172839506173 (81 ratings)
  26. IA: 4.705714285714287 (35 ratings)
  27. OH: 4.701823708206691 (329 ratings)
  28. WA: 4.701818181818172 (165 ratings)
  29. TX: 4.700653061224475 (1225 ratings)
  30. KY: 4.696202531645571 (79 ratings)
  31. LA: 4.694117647058827 (51 ratings)
  32. NV: 4.6935483870967705 (93 ratings)
  33. WI: 4.69055118110236 (127 ratings)
  34. VT: 4.685714285714285 (7 ratings)
  35. FL: 4.682657657657712 (888 ratings)
  36. MI: 4.6805970149253735 (268 ratings)
  37. NC: 4.68034934497815 (229 ratings)
  38. AZ: 4.675581395348846 (344 ratings)
  39. AR: 4.670731707317077 (41 ratings)
  40. NY: 4.66727272727274 (440 ratings)
  41. NH: 4.665000000000001 (80 ratings)
  42. IN: 4.6644808743169275 (183 ratings)
  43. DE: 4.661538461538461 (13 ratings)
  44. IL: 4.650421585160212 (593 ratings)
  45. OR: 4.648648648648649 (37 ratings)
  46. NJ: 4.642136498516329 (337 ratings)
  47. CO: 4.641772151898725 (158 ratings)
  48. GA: 4.604336734693891 (392 ratings)
  49. CA: 4.580988023952118 (668 ratings)
  50. MS: 4.543478260869566 (23 ratings)

  States represented: 50
```

The code also outputs a CSV version of the ranked list ("Average_Car_Reliability_Rating_Per_State.csv"). A copy of this file is located in the root of this repo.

!["ACRRPS_graph.png"](https://raw.githubusercontent.com/ProjectSkyapple/ACM-Research-coding-challenge-22F/d499fa18761a4c70a6c2d7df6451563e03a9aba9/ACRRPS_graph.png)

The code outputs the above graph ("ACRRPS_graph.png"). A copy of this file is located in the root of this repo.

Based on the data above, the 10 states with the *highest* average reliability ratings are:

1. Maine (ME) - 4.8250
2. Nebraska (NE) - 4.8027
3. Alaska (AK) - 4.8000
4. South Dakota (SD) - 4.7870
5. Alabama (AL) - 4.7750
6. Utah (UT) - 4.7740
7. Hawaii (HI) - 4.7563
8. Idaho (ID) - 4.7536
9. Montana (MT) - 4.7500
10. West Virginia (WV) - 4.7462

The 10 states with the *lowest* average reliability ratings are:

41. New Hampshire (NH) - 4.6650
42. Indiana (IN) - 4.6645
43. Delaware (DE) - 4.6615
44. Illinois (IL) - 4.6504
45. Oregon (OR) - 4.6486
46. New Jersey (NJ) - 4.6421
47. Colorado (CO) - 4.6418
48. Georgia (GA) - 4.6043
49. California (CA) - 4.5810
50. Mississippi (MS) - 4.5435

## Sources

## Questions?

If you have any questions or would like to learn more about this project, you can send me a message to aaron.jacob@utdallas.edu.
