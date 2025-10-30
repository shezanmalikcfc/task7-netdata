\# TASK 7 - Monitor System Resources Using Netdata



\## Objective

Install Netdata with Docker and capture dashboard screenshots and running metrics.



\## How I ran Netdata

Used Docker to run Netdata with host mounts:



docker run -d --name=netdata -p 19999:19999 \\

&nbsp; --cap-add SYS\_PTRACE --security-opt apparmor=unconfined \\

&nbsp; -v netdataconfig:/etc/netdata -v netdatalib:/var/lib/netdata \\

&nbsp; -v netdatacache:/var/cache/netdata -v /proc:/host/proc:ro \\

&nbsp; -v /sys:/host/sys:ro -v /etc/os-release:/host/etc/os-release:ro \\

&nbsp; netdata/netdata



\## Files included

\- dashboard.png

\- Container.png

\- docker-stats.png

\- netdata-logs.txt

\- netdata-inspect.txt





\## Notes

Netdata is accessible at http://localhost:19999 (when running locally). Refer to the PNG screenshots for dashboard views.



