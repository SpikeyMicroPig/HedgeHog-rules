# HedgeHog-rules

HedgeHog mod_security rules

Copyright: Kurt Seifried 2015

Author: Kurt Seifried (kurt@seifried.org)

# Overview

These are mod_security rules to address vulnerabilities (CVEs) and hardening in various web based products.

The rules are split into several main categories, first by maturity (effectiveness and safety):

1. Rules that address specific CVEs and are written and tested to not cause false positives, essentially these rules work and will not cause any problems
2. Rules that address specific CVEs and have not been tested or confirmed to not cause false positives, these rules work but may cause problems
3. Rules that address hardening and are written and   tested to not cause false positives, essentially these rules work and will not cause any problems
4. Rules that address hardening	and have not been tested or  confirmed to not cause false positives, these rules work but may cause problems

# tags used in rules

We use the "tag" https://github.com/SpiderLabs/ModSecurity/wiki/Reference-Manual#tag value in rules to identify	them and various aspects of the rule.

The tag format is is "TEXT-STRING-IDENTIFIER/DATA", "TEXT-STRING-IDENTIFIER" must NOT contain a "/" character (the first "/" is the separator). Data can of course contain / characters. I'm not sure how we will handle " characters. Please note for REF we further split and use a second / to seperate fields, e.g. "REF/RHT-ERRATA/RHSA-2015-0001:01" or "REF/RHT-BZ/123456789".

We build rulesets for various products using the CPE data and possibly the CVE data. So a rule may occur in one or more product definitions (e.g. reused components such as xmlrpc.php or timthumb.php can cause this).

## AUTHOR 

may occur one or more times - name/email of rule author

## CPE 

may occur one or more times - CPE(s) this rule applies to

## CVE 

may occur one or more times - CVE(s) this rule applies to

## CWE 

may occur one or more times - Optional CWE data (e.g. 79 is XSS)
may also be a chain of issues (e.g. an XSS then a CSRF), split by commas

## NOTE 

may occur one or more times - Free form text note

## REF 

may occur one or more times - References, e.g. Red Hat Bugzilla link, RHSA, etc. In form vendor abbreviation-identifier/data

## REQUIRES_VERSION

occurs once, specifies the minimum version of mod_security required (e.g. 2.7.3, 2.8.0, 2.9.0)

### RHT-BZ

### RH-ERRATA

# id used in rules

Please note Red Hat has a vendor block from 1,000,000 to 1,009,999
https://github.com/SpiderLabs/ModSecurity/wiki/Reference-Manual#id
