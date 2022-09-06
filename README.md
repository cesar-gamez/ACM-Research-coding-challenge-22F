# ACM Research coding challenge (Fall 2022)

## Project Description/Rationale

Following the start of the COVID-19 pandemic, the used/new car market in the United States experienced a notable increase in purchasing/selling volume. The factors influencing this increase in the car market's volatility was seemingly ambiguous. Therefore, my ACM research project revolved around attempting to predict the factors that most heavily correlate to price volatility (both positively and negatively) within the car market- specifcially using the [cars.com csv dataframe](https://www.kaggle.com/datasets/chancev/carsforsale). Once the highest correlated factors were identified, I chose to visualize them through a [bar chart](https://drive.google.com/file/d/1w8yPcFlOeJERJ8eK0rR3AKsj9aGZJiy0/view?usp=sharing).

## Project Cleanup

The first step in preparing for this project was to reformat any data within the csv file that may have had undesirable prior formatting. The reformatted data included following columns:
"Price"
"Used/New"
"Drivetrain"

### Price Reformat

The original variable-type of the "Price" column was a String. To better read the data, I chose to reformat the string into an integer by removing the currency symbol and commas, then using the pd.astype() method.

### Used/New Refomat

Any new cars within the dataframe were labeled with the format "{Manufacturer}-Certified". To reduce the difference in each of the datapoints, I reformatted all of the rows labelled with this format to "New", thus reducing variability.

### Drivetrain Reformat

Each independent manufacturer had a respective method of defining their car's drivetrain. To reduce variability, I set an integer amount to the "wheel-drive" quantity of the car.

## Correlation/Results

In conclusion, matplotlib and seaborn were both used to find and visualize the correlation between each of the car's datapoints and price. [The following bar chart](https://drive.google.com/file/d/1w8yPcFlOeJERJ8eK0rR3AKsj9aGZJiy0/view?usp=sharing) was the result of the fully processed data. In conclusion, mileage had the greatest inverse relation to price, and year had the greatest direct relation to price.
