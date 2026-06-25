
# Weekly Deliverables

## Week 1 – Orientation & Setup

### Completed Tasks

* Read the project prompt and reviewed project objectives.
* Installed and configured required tools including Python, Git, and Jupyter Notebook.
* Established FTP access through FileZilla.
* Downloaded CRMLS Sold Property data files from the `/raw/California` directory.
* Reviewed the Trestle Property Metadata documentation.

### Dataset Access Confirmation

Successfully obtained access to the CRMLS dataset through the IDX Exchange FTP server. Property data files were downloaded locally and will be used for analysis throughout the project. Raw CSV files are not included in this repository in accordance with project guidelines.

### Key Columns Reviewed

| Column                | Description                                                       |
| --------------------- | ----------------------------------------------------------------- |
| ClosePrice            | Final sale price of the property; target variable for prediction. |
| ListPrice             | Original listing price of the property.                           |
| LivingArea            | Total livable area within the home.                               |
| LotSizeSquareFeet     | Total lot size in square feet.                                    |
| BedroomsTotal         | Number of bedrooms in the property.                               |
| BathroomsTotalInteger | Number of bathrooms in the property.                              |
| YearBuilt             | Year the property was constructed.                                |
| Latitude              | Geographic latitude of the property location.                     |
| Longitude             | Geographic longitude of the property location.                    |
| DaysOnMarket          | Number of days the property was listed before sale.               |
| PropertyType          | General category of the property.                                 |
| PropertySubType       | Specific property classification.                                 |
| CloseDate             | Date the sale was finalized.                                      |

### Initial Observations

Property location, living area, lot size, bedroom count, bathroom count, and property age are expected to be important factors affecting home sale prices. These features will be explored further during data analysis and model development.
