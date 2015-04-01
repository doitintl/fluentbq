# Fluentd Integration with BigQuery, including parsing files and working example for HAproxy
Practical example of configuration files to stream logs with Fluentd and BigQuery plugin based on https://github.com/kaizenplatform/fluent-plugin-bigquery

# Installation Instructions
1. Adjust O/S settings as per http://docs.fluentd.org/articles/before-install
2. Install from repo http://docs.fluentd.org/articles/install-by-deb#step-0-before-installation
3. Install BigQuery plugin `/usr/sbin/td-agent-gem install fluent-plugin-bigquery --no-ri --no-rdoc -V`
4. Create Service Account and download key.p12 file and replace in /etc/td-agent/

# Configuration files
1. Place files from conf.d (in this repo) to /etc/td-agent/conf.d (log source parsing files) 
2. Adjust haproxy.schema file to match your schema (file in repo correlates with conf.d/haproxy.cfg
3. haproxy/haproxy.cfg is here for convinience, providing example for custom log with proper timestamp (unix epoc)
4. rsyslog/rsyslog.conf is just for reference
