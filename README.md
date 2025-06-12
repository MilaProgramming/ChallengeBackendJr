
### 1

You're building a high-throughput API for a cryptocurrency trading platform. For this platform, time is extremely important because microseconds count when processing high-volume trade orders. For communicating with the API, you want to choose the verb that is fastest for read-only operations.  

**What verb should you choose for retrieving trade orders with the API server?**  
**SELECT ONLY ONE**

- [x] 1. GET  
- [ ] 2. UPDATE  
- [ ] 3. DELETE  
- [ ] 4. POST  

A: GET is the standard and most efficient HTTP verb for read-only operations

---

### 2

You work for a Customer Relationship Management (CRM) company. The company's clients gain CRM access through a RESTful API. The CRM allows clients to add contact information for customers, prospects, and related persons (e.g., virtual assistants or marketing directors). You want to choose an appropriate API request path so clients can easily retrieve information for a single contact while also being flexible for future software changes.  

**Which of the following API paths should you use?**  
**SELECT ONLY ONE**

- [ ] 1. /customers/{customer_id}  
- [x] 2. /contacts/{contact_id}  
- [ ] 3. /contacts/{contact_type}/all  
- [ ] 4. /customers/all  

A: This path is resource-oriented, specific for contact rather than ambiguous `customer`, and flexible for future changes to the contacts data model by not depending on any type.

---

### 3

You work for a large social media network, and you've been tasked with error handling for the API. You're trying to decide on an appropriate error code for authentication failures based on non-existent users and incorrect passwords. You want to balance security against brute force attacks with providing descriptive and true error codes.  

**Which HTTP error code(s) should you use to keep the system secure and still report that an error occurred?**  
**SELECT ONLY ONE**

- [ ] 1. 404 if the user doesn't exist, and 403 if the password is wrong.  
- [ ] 2. 403 if the user doesn't exist, and 401 if the password is wrong.  
- [ ] 3. 500 if the user doesn't exist or if the password is wrong.  
- [x] 4. 401 if the user doesn't exist or if the password is wrong.  

A: Returning 401 just means unathorized, so we don't know if the user exists for example, to help with brute force.

---

### 4

You're writing documentation for requesting information about a given user in your system. Your system uses UUIDs (universally unique identifiers) as user identifiers. In your documentation, you want to show an example.  

**True or false: You should put a fake UUID into the example code (instead of just the text "UUID") as a placeholder.**  
**SELECT ONLY ONE**

- [ ] 1. TRUE  
- [x] 2. FALSE  

A: Avoids the risk of accidentally representing real or misleading data in documentation.

---

### 5

You're building code to handle errors issued from a remote API server. The response may or may not have an error.  

**How much work should your method, `handleErrors(response)`, handle?**  
**SELECT ONLY ONE**

- [ ] 1. Check for the presence of an error. If it exists, then set a class property to the error.  
- [x] 2. Check for the presence of an error. If it exists, throw an exception with the error.  
- [ ] 3. Check for the presence of an error. If it exists, set a class property to the error, then throw an exception.  

A: Throwing an exception immediately on error detection ensures that failures are handled explicitly and transparently by consuming code.

---

### 6

You have two classes: a database driver and an email driver. Both classes need to set errors so that your front-end interface displays any errors that transpire on your platform.  

**Which way should you implement this error handling?**  
**SELECT ONLY ONE**

- [ ] 1. Write the error handling the same way in both classes, but keep it to one line of code.  
- [ ] 2. Make a trait to handle errors so it'll collect errors in any class that uses it.  
- [x] 3. Make a driver-based error provider to handle errors in all classes that can issue errors.  

A: A shared error provider to controller level centralizes error handling logic across multiple drivers, promoting consistency and scalability.

---

### 7

You need to name the private method in your class that handles looping through eCommerce products to collect and parse data. That data gets stored in an array and set as a class property.  

**Which of the following should you use to name your method?**  
**SELECT ONLY ONE**

- [ ] 1. loopThroughProductsAndParseData()  
- [ ] 2. loopProductsAndParse()  
- [ ] 3. parseDataForProducts()  
- [x] 4. parseDataForProductsAndSetArray()  

A: Communicates both the action (parsing) and the side effect (setting an array), aligning with descriptive naming best practices.

---

### 8

There are multiple places in your codebase that need to access the database. To access the database, you need to supply credentials. You want to balance security with usability.  

**What strategy should you use to store and access these credentials?**  
**SELECT ONLY ONE**

- [ ] 1. Put them in the code that connects to the database for each place that needs database access.  
- [ ] 2. Put them in a configuration file, then include that file in the code everywhere that needs to access the database.  
- [ ] 3. Put the credentials into a configuration file, then load them with a database service provider.  
- [x] 4. Put them in a `.env` file, load data from it into a configuration system, then request the credentials from a database service provider.

A: This approach separates sensitive credentials from code and supports environment-based configuration.
