# Kali Linux VM Monitoring

## Introduction

This is a repository for monitoring a Kali Linux VM. Monitoring is essential for maintaining system health, identifying performance bottlenecks, and ensuring optimal resource utilization. This guide covers various monitoring tools and commands to track system metrics, including CPU, memory, disk, network, and process usage. 

## For detailed output and options, we can add `--help` after any command.

1. **CPU Load**: Helps in understanding the processing power demands and if they are within the system's capacity.

   -  `top` to see real-time CPU usage
  ![alt text](assets/top.png)
 
    - `htop` for an enhanced view.
  ![alt text](assets/htop.png)

2. **Memory Usage**: show real-time process memory consumption:
   - `free -m` for memory in MB
  ![alt text](assets/free-m.png)
   - `top` to see processes' memory use.

3. **Disk Usage**: Tracks how much storage is being used and available, critical for ensuring data storage does not reach full capacity unexpectedly.

   -  `df -h` shows disk space usage in human-readable format; 
  ![alt text](assets/df-h.png)
   -  `iotop` monitors disk I/O.
  ![alt text](assets/iotop.png) 
1. **Log Files**: Contain detailed system, application, and security events. They are typically found in /var/log/ directory on Linux systems and are crucial for troubleshooting and monitoring system health.

   - Navigate using `cd /var/log/` and view logs with `less syslog` for system logs or with `less auth.log` for authentication logs.
   - Althernatively we can use `journalctl` - to view system logs.
  ![alt text](assets/journalctl.png)
  
1. **User Activity**: The last command can reveal who logged into the system, their activities, and log-off times, providing insights into user behavior and potential unauthorized access.

   - `last` gives a list of last logged-in users.
   ![alt text](assets/last.png)

2. **System Health**: System Health and Performance Metrics: Encompass CPU, memory, disk, and network utilization, along with load averages and process statistics to gauge overall system performance.

   - `vmstat` provides system statistics; 
  ![alt text](assets/vmstat.png)
   - `sensors` for hardware temps.
  ![alt text](assets/sensors.png)
  
1.  **Uptime**: The uptime command shows how long the system has been running since its last restart, indicating stability.

    -  `uptime` tells how long the system's been running.
  ![alt text](assets/uptime.png)
   
1.  **Network Traffic**: Tools like **iftop** or **nethogs** offer insights into real-time network bandwidth usage and traffic patterns, essential for identifying network bottlenecks or suspicious activity.

    -  `iftop` shows network usage.
  ![alt text](assets/iftop.png)
    - Althernatively there is `nethogs` that shows network usage by process.

1. **Process Monitoring**: Tools like **ps** and **pstree** help monitor running processes, their resource consumption, and relationships between them.
  
      -  `ps aux` shows all running processes.
    ![alt text](assets/ps_aux.png)
      -  `pstree` shows processes in a tree format.
    ![alt text](assets/pstree.png)
