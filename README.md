# Hostfully
Hostfully


Property Test Cases
1. POST New Property Without Authentication
Expected Result: 401 Unauthorized must be returned.
2. Create Property
Notes:
- The POST endpoint currently returns 200 OK for success but should return 201 Created.
- According to the specification, only the alias property is required for a property to be created.
   If id is included in the creation object, it is ignored by the application, and a random id is generated instead.

2.1 Fulfill All Properties
    - Expected Result: Creation must succeed. The response object must contain all properties correctly fulfilled.
	
2.2 id Property
	2.2.1 Creation must succeed when id is a valid GUID.
	2.2.3 Creation must fail with 400 Bad Request when id is an invalid GUID (e.g., a random string).

2.3 alias Property
	2.3.1 Creation must succeed when alias is a string.
		- Expected Result: The response object must contain the inserted alias.
	2.3.4 Creation must fail when alias is not included in the object.

2.4 countryCode Property
	2.4.1 Creation must succeed when a single country code is provided.
		- Expected Result: The response object must contain the provided country code.
	2.4.2 Creation must succeed when an array of unique country codes is provided.
		- Expected Result: The response object must contain the array of expected country codes.
	2.4.3 Creation must fail when an array of duplicate country codes is provided.

2.5 createdAt Property
	2.5.1 Creation must succeed when a valid date-time is provided.

2.6 Create a Property with Only the alias Property
   Expected Result: The response object must contain:
    - alias (with the inserted value)
    - id (auto-generated GUID)
    - createdAt (auto-generated date)
    - countryCode (empty or null).
	
Tests that should be covered by Unit tests:
- Propty creation must fail when an array of duplicate country codes is provided.
- Creation must fail with 400 Bad Request when createdAt is an invalid date-time.