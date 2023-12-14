# CustomerAPI_DEMO

1. User Authentication:
   - Send a POST request to `https://qa2.sunbasedata.com/sunbase/portal/api/assignment_auth.jsp` with login credentials.
   - Obtain the Bearer token from the authentication API response.
     
2. Create Customer:
   - Issue a POST request to `https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp` with the Bearer token and customer details.
   - Check for success (status 201) or missing parameters (status 400) in the response.
     
3. Retrieve Customer List:
   - Use a GET request to `https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp`.
   - Include the Bearer token and set the cmd parameter to `get_customer_list`.
   - Receive the list of customer details with a 200 status code.

4. Delete Customer:
   - Send a POST request to `https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp` with cmd set to `delete` and the customer's UUID.
   - Include the Bearer token in the request header.
   - Verify the response status: 200 for success, 500 for an error, and 400 for a missing UUID.

5. Update Customer:
   - Make a POST request to `https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp` with cmd set to `update`.
   - Include the Bearer token, customer's UUID, and updated details in the request body.
   - Check the response for success (status 200), UUID not found (status 500), or an empty body (status 400).
