# Task
- Iterate through the exchange rate data provided
in the json file and display exchange rates for
each country

```python
import json

# Dumped the dictionary data into an exchange_rates.json file
# with open("exchange_rates.json", "w") as jsonfile:
  #   json.dump(exchange_rate_date, jsonfile)

with open("exchange_rates.json") as jsonfile:
	exchange_rate_data = json.load(jsonfile)
	#print(exchange_rate_data)

# Creating the exchange rate class
class Exchange_Rate:
    # This function iterates through each item in the subdictionary of 'rates' within the
	# json file, and outputs both the country and exchange rate
	def exchange_rate(self):
		print("The exchange rates for each country are:\n --> ")
		for i, j in exchange_rate_data['rates'].items():
			print(f"{i.upper()}: {j}")


# Making sure the files are run after everything is stored in RAM
def main():

	# Calling an object of the class
	test = Exchange_Rate()

	# Testing functionality of the exchange_rate method which displays exchange rate
	test.exchange_rate()

if __name__ == '__main__':
    main()
```