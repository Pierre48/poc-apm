FROM splunk/universalforwarder:latest
COPY src/custom-splunkuniversalforwarder/outputs.conf /opt/splunkforwarder/etc/system/local/outputs.conf
RUN sudo chmod 777 /opt/splunkforwarder/etc/system/local/outputs.conf
RUN sudo mkdir /opt/splunkforwarder/etc/apps
RUN sudo wget "https://cdn.apps.splunk.com/media/private/815807e2-80c7-11e8-9554-02f13bdc2585.tgz?response-content-disposition=attachment%3Bfilename%3D%22prometheus-metrics-for-splunk_060.tgz%22&Expires=1616537363&Signature=n2rzLRx8TgSLbhMc8m6P5MrwWnzLomVmOAp2GtbGesj2xGgV~EnkEuUkRwzjI5r9HRYEwDshu7PGg3Ixvcztb~1AGmobyxRi4dtafv28rmfv0ve31KTJIsmc8Mm7ERIph9cUlEn3syEUXwJQrDv94X7GG0hkNSdZKm4iHElAg6Mh0YbQJwXGpVMb0FBdHa8INqz4ae61uz0neek7RBtzYdB55YzzteoEHuG5upkGDosL0Z3ORtdRa3Q189t7h9xVFuHG~0deUzq62alnPIcg5sRHJZboJLND1kHqiMkIcgwsg-LPxvIvNjFOMNmlZ3PQaXVgt0EaI006VLu4in0CIA__&Key-Pair-Id=APKAISM7Q7KZPNKOIT7A" -O prom.tgz
RUN sudo tar -zxvf /opt/splunkforwarder/etc/apps/prom.tgz
