# Smart-Irrigation
**Using an Artificial Neural Network along with an IoT device to check whether irrigation is required by the crops or not.**

**Reading the data from the CSV file keeping the required data and dropping unnamed files.**


---



*Information about the data*
*  There are 20 sensors.
*  There are 3 types of crops.


---



*Assumptions*
*  We have FC-28 sensors, which are scattered all round our crop field(FC-28 is a type of soil moisture sensor).
*  We have a nodeMCU.




# Real Time data



*   Real time data is provided by the sensors.
*   That data is converted into a csv file one of googles' API's, and this is the code for the following.

```
# import requests
url = "https://sheets.googleaps.com/v4/spreadsheets/{spreadsheetId}/values/{sheetname}!range{range}?alt=csv"
response = requests.get(url)
with open("sheet.csv", "wb) as f:
  f.write(response.content)
```

*   This is a code that will be used to convert the data into a csv file which will be fed further into our ANN model.
