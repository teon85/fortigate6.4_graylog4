# fortigate6.4_graylog4
Content pack for fortigate to graylog

Tested with Fortigate 601E FortiOs V6.4.4 build 1803  and graylog 4.0.2

Source fortiOS 6.4.4 https://docs.fortinet.com/document/fortigate/6.4.4/fortios-log-message-reference/524940/introduction

Inspired from https://github.com/pfitchie/graylog3.Fortigate6xContentPack


Setup Notes
Input is for FortiGate Firewall with Raw/Plaintext UDP.

Import the Content Pack
Update the search,alert,stream and dashboard rule with your device gl2_source_input serial.
Point FortiGate syslog to Graylog with cli command :
  config log syslogd setting
    set status enable
    set server "172.30.1.7"
    set port 1500
    set priority low
  end

  config log syslogd filter
    set severity warning
  end
