**Get data from API**

• **API**:
- **Application Programming Interface**
- **interfaces provided by servers** that can be used **to retrieve and send data** using code
- allows **software applications to communicate** with each other via API calls   
- **streamlines complex instructions** to provide back a request from a server
- provides **efficiencies over using static data downloads** (e.g. CSV):
	- working with **rapidly changing data**
	- working with **data from which you only want a small chunk**

• **API data**:
- **gathering** data:
	- without requiring authentication
	- with requiring authentication
- **add** data **into Pandas DataFrame**

• **Requests library**
  
  - most common **library for making requests and working with APIs**
  - used to **pull / retrieve data from an API using Python**
  - standard **package for making HTTP requests** in Python
  - not part of the standard Python package and need to be installed

• **Steps**:

**1. Obtain API secret key**
  - used **only when authentication** is required
  - allows **user to be authenticated** without needing to provide username and password

**2. Import the Libraries**
  - **Pandas** library
  - **Requests** library
  - **JSON** library

**3. Generate URL request, access its status code attribute and access data**
  - **API request**:
    - **make a request**:
      	- contains **data regarding API request call**
      	- **made up of 4 pieces**: Endpoint, Method, Header, Data / Body
    - returns response object which includes:
      	- **request status code** is a value that tells what happened with the request
      	- **data to access** / extract that usually comes back in JSON format (Key-Value pairs)

**4. Convert JSON string into Python object (Dictionary)**
  - use **json.dumps()** method that **serializes Python object to a JSON formatted string using conversion table**

**5. Parse data out**
  - use **JSON response of the JSON object of the result** (response_json variable)

**6. Add Data into Pandas DataFrame**
  
  - use **pd.DataFrame()** to create DataFrame object from a Numpy ndarray, dictionary or dataclass
  - use **pd.DataFrame.from_records()** to create DataFrame object from a structured or record ndarray, list of tuples or dicts, or DataFrame
  - use **pd.DataFrame.from_dict()** to create DataFrame object from dictionary of array-like or dictionaries by columns or by index allowing dtype specification
  - use **pd.json_normalize()** to create DataFrame object from semi-structured JSON data (Nested data - lists of dictionaries (records) or nested dictionaries)
