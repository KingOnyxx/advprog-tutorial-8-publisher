a. it will send 5 data to the message broker in one run because there are 5 publish_event methods.
<br>
<br>
b. Both url are the same because both send request to the same rabbitMQ server. The only difference is publisher will send message to the queue and subscriber will receive data from the queue.