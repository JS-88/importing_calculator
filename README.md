Import Cost Calculator
This Import Cost Calculator is a simple web-based tool designed to help users calculate and manage the total landed cost of imported goods, including detailed breakdowns of shipping, import costs, duties, and VAT. Users can enter relevant data, view a summary, save calculations for future reference, and reload or delete previous entries as needed.

Features
Exchange Rate Entry: Enter a USD to GBP exchange rate for accurate currency conversions.
Shipping & Import Costs Section: Fields for freight, port handling, container fees, and insurance.
Import Duties & Taxes Section: Fields for customs duty rates, import VAT, and broker fees.
Detailed Summary Section: Displays individual line items and a grand total for all costs in both USD and GBP.
Save Calculations: Users can name and save calculations to the browser’s local storage for later use.
Load and Delete Saved Calculations: Access previous calculations by name, with the ability to load data back into the calculator or delete unwanted entries.

Requirements
A modern web browser (e.g., Chrome, Firefox, Safari, Edge) that supports JavaScript and HTML5 Local Storage.
Usage

1. Setting Up and Running
Download or clone the project file import_cost_calculator.html.
Open the file in a web browser by double-clicking it or dragging it into the browser.
2. Using the Calculator
Exchange Rate: Start by entering the current USD to GBP exchange rate in the Exchange Rate section.
Shipping & Import Costs: Enter the relevant amounts for freight, port handling, container fees, and insurance in the Shipping & Import Costs section.
Import Duties & Taxes: In the Import Duties & Taxes section, enter customs duty rates, import VAT, and broker fees as applicable.
Summary: The Summary section automatically calculates line-by-line totals and a grand total for USD and GBP based on your entries.
3. Saving and Managing Calculations
   
Saving a Calculation:

In the Summary section, enter a name for your calculation and click Save Calculation.
Your calculation will appear in the Saved Calculations list below.
Loading a Calculation:
Click on a saved calculation in the Saved Calculations list to load it back into the form.
Deleting a Calculation:
Click the Delete button next to a saved calculation to permanently remove it.
Project Structure
This project is a single HTML file with embedded CSS and JavaScript, allowing for easy portability and usage in any modern web browser.

License
This project is licensed under the MIT License. See LICENSE for more information.


Sliders:
Weight Factor Slider: Controls how much weight contributes to the shipping cost. This is represented as a percentage.
Volume Factor Slider: Controls how much volume contributes to the shipping cost. This is also represented as a percentage.
Both sliders combined must always add up to 100%. If the weight factor is increased, the volume factor will decrease automatically, and vice versa.

Logic and Formulas:
Total Shipping Costs:
This is the sum of all the shipping-related costs:

Total Shipping Costs
=
Freight
+
Port Handling
+
Container Fees
+
Insurance
Total Shipping Costs=Freight+Port Handling+Container Fees+Insurance
Contribution of Each Product to Total Shipment:
For each product, we calculate how much it contributes to the total shipment in terms of weight and volume:

Weight Contribution:

The product’s weight compared to the total shipment weight.
Formula:
Weight Contribution
=
Product Weight
Total Shipment Weight
Weight Contribution= 
Total Shipment Weight
Product Weight
​
 
Volume Contribution:

The product’s volume compared to the total shipment volume.
Formula:
Volume Contribution
=
Product Volume
Total Shipment Volume
Volume Contribution= 
Total Shipment Volume
Product Volume
​
 
These contributions will help determine how much of the shipping cost is assigned to each product based on weight and volume.

Applying the Sliders:
Weight Factor: This is the percentage of the shipping cost that is allocated based on the product’s weight.
Volume Factor: This is the percentage of the shipping cost that is allocated based on the product’s volume.
These factors represent how much of the shipping cost is attributed to weight vs. volume. For example, if the Weight Factor is set to 70%, 70% of the shipping cost will be allocated based on the product’s weight and 30% based on volume.

Shipping Cost Allocation per Unit:
We now calculate how much shipping cost is allocated to each unit of the product, based on both the weight and volume contributions.

Shipping Cost per Unit
=
(
Weight Contribution
×
Weight Factor
+
Volume Contribution
×
Volume Factor
)
×
Total Shipping Costs
Quantity of Product
Shipping Cost per Unit=(Weight Contribution×Weight Factor+Volume Contribution×Volume Factor)× 
Quantity of Product
Total Shipping Costs
​
 
Weight Contribution: How much the product's weight compares to the total shipment weight.
Volume Contribution: How much the product's volume compares to the total shipment volume.
Weight Factor and Volume Factor are percentages that determine how much shipping cost is based on weight and volume.
The total shipping costs are multiplied by the weighted sum of these contributions.
Example:
Let's assume:

Product weight = 500 kg
Product volume = 2 cubic metres
Total shipment weight = 1000 kg
Total shipment volume = 10 cubic metres
Total shipping costs = $1000
Weight factor = 70% and volume factor = 30%
Quantity of the product = 100 units
Now, we calculate:

Weight Contribution:
Weight Contribution
=
500
 
kg
1000
 
kg
=
0.5
Weight Contribution= 
1000kg
500kg
​
 =0.5
Volume Contribution:
Volume Contribution
=
2
 
m
3
10
 
m
3
=
0.2
Volume Contribution= 
10m 
3
 
2m 
3
 
​
 =0.2
Shipping Cost per Unit:
Shipping Cost per Unit
=
(
0.5
×
0.7
+
0.2
×
0.3
)
×
1000
100
Shipping Cost per Unit=(0.5×0.7+0.2×0.3)× 
100
1000
​
 
Breaking this down:

Shipping Cost per Unit
=
(
0.35
+
0.06
)
×
10
=
0.41
×
10
=
4.10
 
USD per unit
Shipping Cost per Unit=(0.35+0.06)×10=0.41×10=4.10USD per unit
This means that $4.10 of the shipping cost is allocated to each unit of the product based on its weight and volume contributions, according to the sliders.

Final Landed Cost per Unit:
Once the shipping cost per unit is calculated, the final landed cost per unit includes other costs like the unit price, VAT, and miscellaneous costs:

Landed Cost per Unit
=
Unit Price
+
VAT
+
Miscellaneous Costs
+
Shipping Cost per Unit
Landed Cost per Unit=Unit Price+VAT+Miscellaneous Costs+Shipping Cost per Unit
The shipping cost per unit is determined by the product’s contribution to the shipment’s weight and volume, and the sliders help determine how much weight vs. volume should influence the shipping cost.
