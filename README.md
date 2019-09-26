# prometheus-doc


Moniroting :

## Means are you are been watched.

Monitoring
Collecting, processing, aggregating, and displaying real-time quantitative data about a system, such as query counts and types, error counts and types, processing times, and server lifetimes.

White-box monitoring
Monitoring based on metrics exposed by the internals of the system, including logs, interfaces like the Java Virtual Machine Profiling Interface, or an HTTP handler that emits internal statistics.

Black-box monitoring
Testing externally visible behavior as a user would see it.

Dashboard
An application (usually web-based) that provides a summary view of a service’s core metrics. A dashboard may have filters, selectors, and so on, but is prebuilt to expose the metrics most important to its users. The dashboard might also display team information such as ticket queue length, a list of high-priority bugs, the current on-call engineer for a given area of responsibility, or recent pushes.

Alert
A notification intended to be read by a human and that is pushed to a system such as a bug or ticket queue, an email alias, or a pager. Respectively, these alerts are classified as tickets, email alerts,22 and pages.


So, let’s dive into SRE’s golden signals and see why monitoring them is essential to the reliability of any system.

Latency: How long does it take to service a request? Define a benchmark for the latency associated with successful requests and monitor that against the latency of failed requests. Tracking the latency of errors allows you to address any concerns around the speed of identifying an incident and how quickly you can dive into incident response.

Traffic: Traffic is fairly self-explanatory. How much stress is your system taking on from the number of users or transactions running through your service? Depending on the functionality of your service, measuring traffic can look quite different from company to company. By monitoring real-user interactions and traffic you can better understand the way end-users experience your service and create visibility into how your systems hold up under stress.

Errors: Of course, every team needs to monitor for errors. Whether those errors are defined based on manually defined logic or they’re explicit errors such as a failed HTTP request, SRE teams need to monitor for them. Many SRE teams use incident management software to alert on critical errors, take action to identify why an error is happening, and work toward incident remediation.

Saturation: Every team needs to monitor the utilization of their system. It’s important for SRE teams to define a metric for saturation that means the service is maxed out. Most services start to degrade before utilization hits 100%, so understanding the functionality of your own system is important to defining a saturation benchmark that makes sense.



## Architecture overview

![](https://cdn.jsdelivr.net/gh/prometheus/prometheus@c34257d069c630685da35bcef084632ffd5d6209/documentation/images/architecture.svg)
