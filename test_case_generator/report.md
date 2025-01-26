### TEST CASE: User Provisioning Through API Integration  
## Preconditions:  
- API keys are configured.  
- The relevant endpoint for user provisioning is accessible.  

## Steps:  
1. Send a POST request to the user provisioning API endpoint with the following details:  
   - Name: "John Doe"  
   - Email: "johndoe@example.com"  
   - Role: "User"  
2. Capture the response from the API.  
3. Validate the HTTP response status code is 201 (Created).  
4. Verify the response body contains a success message and includes the newly created user ID.  

## Expected Result:  
- A new user "John Doe" is created successfully in the Sailpoint system.  
- The API response returns a success status (201) along with relevant user details, indicating that the user provisioning process was successful.