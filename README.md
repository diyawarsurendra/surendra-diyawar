# surendra-diyawar
#!/bin/bash echo "===== SERVER HEALTH REPORT =====" echo "Hostname : $(hostname)" echo "Uptime   : $(uptime -p)"  echo "---- CPU ----" top -bn1 | grep "Cpu(s)"  echo "---- MEMORY ----" free -h  echo "---- DISK ----" df -h | grep -E '^/dev'  echo "---- TOP 5 MEMORY PROCESSES ----" ps aux --sort=-%mem | head -6  echo "Report generated on $(date)"
