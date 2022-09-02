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

## Conclusion

(In the works.)

## Sources

## Questions?

If you have any questions or would like to learn more about this project, you can send me a message to aaron.jacob@utdallas.edu.
