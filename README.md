# lf

Collection of handy tools for pentesting or CTF.

## LFadwizard

Wizard of https://orange-cyberdefense.github.io/ocd-mindmaps/ (2023 version), allowing to search among commands and define variables.

```
LFadwizard
  intel           # show predefined variables
  ip = 127.0.0.1  # variable definition
  blocks          # categories
  block no        # print block starting with "no"
  impacket        # search by tool
  1433            # search by port
  hot             # show by tags (the best commands)
```

## LFbloodhound

CLI parses of BloodHound outputs, when running GUI is inconvenient.

```
LFbloodhound --help                            # description of various properties
LFbloodhound bloodhound.zip                    # list of domain, computer, user and group objects
LFbloodhound bloodhound.zip --domains          # detailed view of domains
LFbloodhound bloodhound.zip --computers        # detailed view of computers
LFbloodhound bloodhound.zip --users            # detailed view of users
LFbloodhound bloodhound.zip --groups           # detailed view of groups
LFbloodhound bloodhound.zip 1001-1005          # example of filtering with RID
```

## LFcves

Searching of CVEs for products and their versions.

```
LFcves CVE-2014-0160
LFcves apache http_server 2.4.14
LFcves cpe:2.3:a:f5:nginx:1.14.0
LFcves list.txt
```

## LFenumwizard

Wizard for enumeration and reconnaisance stage, very early version.

## LFgroupby

Group by for CSV files and basic statistics

```
cat /etc/passwd | LFgroupby -d : -i 1,2,3,4,5,6  # count usage of shells
cat access.log | LFgroupby -d ' ' -f 1,6         # statistics by IP and method
```

## LFhashalgo

Tries all JTR's formats and subformats against known password and its hash.

```
./LFhashalgo password 696d29e0940a4957748fe3fc9efd22a3
[-] LM
[-] dynamic_n
...
[-] ZipMonster
[-] dynamic_0
[+] dynamic_2
[-] dynamic_3
...
```


## LFhtml

Quick parser of HTML structure.

```
curl -4 https://wordpress.com | LFhtml  

Links:
[a]      https://wordpress.com/                                                    1074           
[a]      https://wordpress.com/pricing/                                            1094  Plans & Pricing
[a]      https://wordpress.com/log-in/                                             1101  Log in   
[form]   https://wordpress.com/start/domain/domain-only/                           1560           
[img]    https://wordpress.com/wp-content/uploads/2023/06/group-1000004724.png     1409           
[img]    https://wordpress.com/wp-content/uploads/2023/06/play-store-logo.png      1414           
[img]    https://wpcom.files.wordpress.com/2025/10/rating-icon402x.png             1434           
[script] /home.logged-out/page-2024-jul/js/bundle.js?v=1753350210                  1999           
[script] /wp-content/js/bilmur.min.js?i=17&m=202550                                2290
[link]   //s1.wp.com                                                               11             
[link]   //fonts.gstatic.com                                                       12             
...

Comments:
<!--  .lp-hero-background.lp-hero-background-plus  -->
<!--  $12  -->
<!--  Intentionally left empty  -->
<!--  wpcom_wp_footer  -->
<!--  A8C Analytics [start]  -->
<!--  A8C Analytics [end]  -->
<!--  CCPA [start]  -->
<!--  CCPA [end]  -->

Emails:
privacypolicyupdates@automattic.com

```

