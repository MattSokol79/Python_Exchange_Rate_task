# Task
- In this instance we will be using a JSON file with exchange rates
- Build your class around it
- You will see from the exchange rates file that you will be accessing 
these data points as you would in a dictionary
- Iterate through the exchange rate data provided
in the json file and display exchange rates for
each country


## Acceptance Criteria
- Create a new repo
- .gitignore and README in a new project
- Have the exchange_rates.json file in the project
folder
- Display all the data from .json file
- Iterate through the data and display 
exchange rate by country

### Task Complete
- First need to import json and make sure the json
file is available in the folder
```python
import json

# Dumped the dictionary data into an exchange_rates.json file:
# with open("exchange_rates.json", "w") as jsonfile:
  #   json.dump(exchange_rate_date, jsonfile)

# Stored the json data into a variable so that it can be used like a normal dict
with open("exchange_rates.json") as jsonfile:
	exchange_rate_data = json.load(jsonfile)
	#print(exchange_rate_data)
```
- Then create the class with methods to display exchange
rates
```python
# Creating the exchange rate class
class Exchange_Rate:

	# This function iterates through each item in the sub-dictionary of 'rates' within the
	# json file, and outputs both the country and exchange rate
	def exchange_rate(self):
		print("The exchange rates for each country are:\n --> ")
		for i, j in exchange_rate_data['rates'].items():
			print(f"{i.upper()}: {j}")
```

- Finally call an object of the class and test the
functionality of the method
```python
# Making sure the files are run after everything is stored in RAM
def main():

	# Calling an object of the class
	test = Exchange_Rate()

	# Testing functionality of the exchange_rate method which displays exchange rate
	test.exchange_rate()

if __name__ == '__main__':
    main()
```