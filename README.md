a. it will send 5 data to the message broker in one run because there are 5 publish_event methods.
<br>
<br>
b. Both url are the same because both send request to the same rabbitMQ server. The only difference is publisher will send message to the queue and subscriber will receive data from the queue.
![rabbit dashboard](image1.png)
![alt text](image2.png)
this screenshot shows that the publisher send 5 data to the queue.
![alt text](image3.png)
this screenshot shows that the chart has some spikes because the publisher has run multiple times.

Things to improve this code:
- Error Handling: The unwrap() method is used, which can cause the program to panic if the Result is an Err. It's better to handle these potential errors gracefully.
- Hardcoded Values: The connection string, event name, and user data are hardcoded. It would be better to move these to a configuration file or environment variables.
- Code Duplication: The publish_event method is called multiple times with similar data. This could be refactored into a loop that iterates over a list of users.
- Unimplemented Function: The get_handler_action function is not implemented and just has a todo!() call. This should be implemented or removed if not needed.