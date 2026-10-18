
# Container Observability Report

## 1. Application Logs

I retrieved the Nginx application logs using the `docker logs client-website` command. The logs show the HTTP requests received by the web server and the response status codes returned to the client.

### Failed Request (HTTP 404)

The following response was returned when I requested a page that does not exist:

```html
<html>
<head><title>404 Not Found</title></head>
<body>
<center><h1>404 Not Found</h1></center>
<hr><center>nginx/1.31.7</center>
</body>
</html>
```

The Nginx server returned a 404 Not Found response because the requested `/hidden-admin-page` resource does not exist. Application logs are important because they help engineers identify failed requests, investigate errors, and understand what happened when users encountered a problem.

## 2. Real-Time Container Metrics

I used the `docker stats client-website` command to observe the container's resource consumption.

- **Memory Usage:** 2.754MiB / 1.859GiB
- **CPU Percentage:** 0.00%
- **Network I/O:** 3.73kB / 5.25kB

## 3. Observations

The Docker metrics provide a snapshot of the container's resource consumption. These measurements help an engineer determine whether the container is using excessive CPU or memory and whether further investigation is needed.
