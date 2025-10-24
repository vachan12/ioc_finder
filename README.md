# ioc_finder
This is a automation python script which can be used for searching for Indicators of Compromise (IOCs) within a dump of logs.

USAGE:

# Basic - just console output
python ioc_analyzer.py /path/to/logs --ip 192.168.1.100

# Save report to file
python ioc_analyzer.py /path/to/logs --ip 192.168.1.100 -o report.txt

# With IOC file and save report
python ioc_analyzer.py /path/to/logs -i iocs.json -o detailed_report.txt

# Full example with multiple IOCs
python ioc_analyzer.py /home/user/backup_logs \
    --ip 10.0.0.5 \
    --ip 192.168.1.100 \
    --domain malicious.com \
    --filename malware.exe \
    -o ioc_findings.txt
```

**Command Structure:**
```
python ioc_analyzer.py <LOG_DIRECTORY> [OPTIONS]

Required:
  <LOG_DIRECTORY>     Path to folder containing logs

Options:
  -i, --ioc-file      IOC file (JSON or text)
  -o, --output        Save report to this file
  --ip                IP address to search
  --domain            Domain to search
  --filename          Filename to search
