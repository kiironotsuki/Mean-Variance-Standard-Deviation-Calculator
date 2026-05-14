# Mean-Variance-Standard-Deviation-Calculator

A self-contained Python utility that leverages NumPy to output a variety of statistical metrics for a $3 \times 3$ matrix. This project is designed for quick data analysis, providing calculations for rows, columns, and the flattened matrix.FeaturesAutomatic Reshaping: Converts a list of 9 digits into a structured $3 \times 3$ array.Comprehensive Stats: Calculates Mean, Variance, Standard Deviation, Max, Min, and Sum.Axis-Specific Results: Outputs data formatted for Axis 0 (columns), Axis 1 (rows), and the total matrix.Zero External Dependencies (Local): The NumPy import is encapsulated within the function for maximum portability.Logic OverviewThe calculator treats the input list as a matrix, where calculations are performed across different dimensions:Axis 0: Vertical calculations (Column-wise).Axis 1: Horizontal calculations (Row-wise).Flattened: The calculation for all 9 elements combined.UsagePrerequisitesPython 3.xNumPyBashpip install numpy
Quick StartYou can call the calculate function by passing a list containing exactly nine numbers:Pythonfrom mean_var_std import calculate

results = calculate([0, 1, 2, 3, 4, 5, 6, 7, 8])
print(results)
Example OutputWhen providing the input [0, 1, 2, 3, 4, 5, 6, 7, 8], the function returns:JSON{
  "mean": [[3.0, 4.0, 5.0], [1.0, 4.0, 7.0], 4.0],
  "variance": [[6.0, 6.0, 6.0], [0.66, 0.66, 0.66], 6.66],
  "standard deviation": [[2.44, 2.44, 2.44], [0.81, 0.81, 0.81], 2.58],
  "max": [[6, 7, 8], [2, 5, 8], 8],
  "min": [[0, 1, 2], [0, 3, 6], 0],
  "sum": [[9, 12, 15], [3, 12, 21], 36]
}
Error HandlingThe function includes a ValueError check to ensure the input list contains exactly nine elements, preventing reshaping errors before they occur.
