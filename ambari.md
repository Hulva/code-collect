# ambari issues

## ambari ssl certificate_verify_failed

* /etc/python/cert-verification.cfg `verify=platform_default` -> `verify=disable`
  * > `sed -i 's/verify=platform_default/verify=disable/' /etc/python/cert-verification.cfg`
* /etc/ambari-agent/conf/ambari-agent.ini
  * > 在 [security] 下  `force_https_protocol=PROTOCOL_TLSv1_2`
