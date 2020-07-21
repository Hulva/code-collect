# ambari issues

## ambari ssl certificate_verify_failed

* /etc/python/cert-verification.cfg `verify=platform_default` -> `verify=disable`
  * > `sed -i 's/verify=platform_default/verify=disable/' /etc/python/cert-verification.cfg`
* /etc/ambari-agent/conf/ambari-agent.ini
  * > 在 [security] 下  `force_https_protocol=PROTOCOL_TLSv1_2`
## [Errno -1] Package does not match intended download. Suggestion: run yum --enablerepo=ambari-2.6.2.2 clean metadata

在这之前应该有这一句 `Delta RPMs disabled because /usr/bin/applydeltarpm not installed.`

SOLVE: `yum install deltarpm`
