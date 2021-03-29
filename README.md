# Icinga2-Pushover-Plugins

## I. DESCRIPTION:

Pushover notification plugins for Icinga2

Copyright (c) 2021 Frostbyte <frostbytegr@gmail.com>

## II. CREDITS:

* brian@aljex.com - url encode function
* info@icinga.com - sample code and formatting for notification plugins

## III. USAGE:

* pushover-host-notification.sh -k <pushover_user_key> -p <pushover_api_token> -t \$notification.type\$ -l \$host.name\$ -n \$host.display_name\$ -s \$host.state\$ -o \$host.output\$ -d \$icinga.long_date_time\$ [ -4 \$address\$ ] [ -6 \$address6\$ ] [ -b \$notification.author\$ ] [ -c \$notification.comment\$ ] [ -i \$notification_icingaweb2url\$ ] [ -v ]
  - example: pushover-host-notification.sh -k 1234567890abcdefghijklmnopqrst -p 1234567890abcdefghijklmnopqrst -t "Recovery" -l "zawarudo.jojos" -n "zawarudo" -s "OK" -o "PING OK - Packet loss = 0%, RTA = 0.40 ms" -d "0000-00-00 00:00:00 +0200" -4 "192.0.2.1" -6 "2001:db8::1" -b "Dio Brando" -c "You were expecting a comment, but it was me, Dio!" -i "http://127.0.0.1/icingaweb2" -v
* pushover-service-notification.sh -k <pushover_user_key> -p <pushover_api_token> -t \$notification.type\$ -l \$host.name\$ -n \$host.display_name\$ -e \$service.name\$ -u \$service.display_name\$ -s \$service.state\$ -o \$service.output\$ -d \$icinga.long_date_time\$ [ -4 \$address\$ ] [ -6 \$address6\$ ] [ -b \$notification.author\$ ] [ -c \$notification.comment\$ ] [ -i \$notification_icingaweb2url\$ ] [ -v ]
  - example: pushover-service-notification.sh -k 1234567890abcdefghijklmnopqrst -p 1234567890abcdefghijklmnopqrst -t "Recovery" -l "zawarudo.jojos" -n "zawarudo" -e "ssh" -u "SSH" -s "OK" -o "SSH OK - OpenSSH_8.0 (protocol 2.0)" -d "0000-00-00 00:00:00 +0200" -4 "192.0.2.1" -6 "2001:db8::1" -b "Dio Brando" -c "You were expecting a comment, but it was me, Dio!" -i "http://127.0.0.1/icingaweb2" -v

NOTE: Plugin outputs can be tested locally by manually supplying the values and the -v (verbose output) argument. If you don't want it to count towards your monthly message limit, simply provide an incorrect user key and api token.
