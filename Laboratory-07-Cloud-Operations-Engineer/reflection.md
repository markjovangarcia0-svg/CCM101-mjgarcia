
# Mission 7 Reflection

This laboratory activity helped me understand that cloud operations involve more than deploying an application. An application may be running, but an engineer still needs to monitor the host server and check whether its resources are sufficient. Monitoring RAM, disk space, and CPU activity helps identify possible problems before they affect users.

Checking host resources is important because Docker containers depend on the server where they run. If the host runs out of memory or disk space, the containers may become slow or stop working correctly. In this activity, I checked the server's memory and disk capacity to establish a baseline before examining the web server.

The `docker logs` command is useful when a user reports a problem, such as being unable to access a web page. It allows an engineer to inspect recorded requests and identify errors, including HTTP status codes. In this activity, I requested a nonexistent page and received a 404 Not Found response. This demonstrated how an intentional error can help me understand the information available for troubleshooting.

I also learned that logs and metrics provide different kinds of information. Logs describe events and requests handled by an application, while metrics show numerical measurements such as CPU usage, memory consumption, and network activity. Both are useful because logs help explain what happened, while metrics help show how the system is performing.

Large companies can monitor thousands of containers using centralized tools such as Prometheus and Grafana. Prometheus collects and stores monitoring data, while Grafana presents the information through dashboards. Alerts can help engineers notice unusual resource usage and respond to problems more quickly.

Overall, this activity improved my ability to use Linux commands, deploy an Nginx container, test HTTP responses, and inspect application logs. I also learned that reliable troubleshooting depends on collecting actual evidence, recording accurate measurements, and using the results to make informed decisions.
