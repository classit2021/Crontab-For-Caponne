#0 1 * * * /usr/bin/find /PATH/logs -maxdepth 1 -name "*.log.????-??-??" -type f -mtime +1 -exec gzip {} \;
#1 1 * * * /usr/bin/find /PATH/logs -maxdepth 1 -name "*????-??-??.log" -type f -mtime +1 -exec gzip {} \;
#
#0 2 * * * /usr/bin/find /PATH/logs -maxdepth 1 -name "*.log.????-??-??.gz" -type f -mtime +10 -exec rm -f {} \;
#1 2 * * * /usr/bin/find /PATH/logs -maxdepth 1 -name "*????-??-??.log.gz" -type f -mtime +10 -exec rm -f {} \;
