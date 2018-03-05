# beast-check
beast.pl - SSL/TLS BEAST Vulnerability Check

A small perl script that checks a target server whether it is prone to BEAST vulnerability via target preferred cipher. It assumes no workaround (i.e. EMPTY FRAGMENT) applied in target server. Some sources said this workaround was disabled by default for compatibility reasons. This may be the reason why RC4 ciphersuite was widely chosen as highest preferred ciphersuite for the primary workaround.

```

$ ./beast.pl

===============================================

SSL/TLS BEAST Vulnerability Check by YGN Ethical Hacker Group, http://yehg.net/

===============================================

Usage: beast.pl host [port]

port = 443 by default {optional}

```

``` $ ./beast.pl www.hotmail.com

===============================================

SSL/TLS BEAST Vulnerability Check by YGN Ethical Hacker Group, http://yehg.net/

===============================================

Target: www.hotmail.com:443

The target is PRONE to BEAST attack.
Protocol: TLS v1 Server Preferred Cipher: AES128-SHA Vulnerable: YES

```

``` $ ./beast.pl www.google.com

===============================================

SSL/TLS BEAST Vulnerability Check by YGN Ethical Hacker Group, http://yehg.net/

===============================================

Target: www.google.com:443

The target is NOT vulnerable to BEAST attack.
Protocol: TLS v1 Server Preferred Cipher: ECDHE-RSA-RC4-SHA Vulnerable: NO