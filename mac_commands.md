## Knowing connected network name from terminal
/Sy*/L*/Priv*/Apple8*/V*/C*/R*/airport -I | awk '/ SSID:/ {print $2}'

## ssh'ing in mac terminal
ssh user@IP-Address

Replace user and IP-Address with the username and IP on the remote server. Hit return to execute the command.
