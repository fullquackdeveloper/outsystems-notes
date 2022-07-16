# Logging levels reference for integrations

* Default - Information is only logged for requests with errors.
* Troubleshoot - Information is only logged for requests with errors, along with additional HTTP trace information.
* Full - All requests/responses are logged, including additional HTTP trace information.

Increasing logging level implies that:
* More information gets logged, increasing the amount of information stored in the environment's database.
* The platform logs input and output parameter values along with the request, thus making any sensitive information present in these parameters available through the environment management console.

Note: For consumed REST APIs, you can redact input parameter values from the logs.