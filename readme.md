Nettacker
=========
[![Build Status Travic CI](https://travis-ci.org/viraintel/OWASP-Nettacker.svg?branch=master)](https://travis-ci.org/viraintel/OWASP-Nettacker)
[![Python 2.x](https://img.shields.io/badge/python-2.x-blue.svg)](https://travis-ci.org/viraintel/OWASP-Nettacker)
[![Python 3.x](https://img.shields.io/badge/python-3.x-blue.svg)](https://travis-ci.org/viraintel/OWASP-Nettacker)
[![Apache License](https://img.shields.io/badge/License-Apache%20v2-green.svg)](https://github.com/viraintel/OWASP-Nettacker/blob/master/LICENSE)
[![Executed](http://nettacker.z3r0d4y.com/update_counter.py)](https://github.com/viraintel/OWASP-Nettacker/)
[![Twitter](https://img.shields.io/badge/Twitter-@iotscan-blue.svg)](https://twitter.com/iotscan)


***THIS SOFTWARE WAS CREATED FOR AUTOMATED PENETRATION TESTING AND INFORMATION GATHERING. CONTRIBUTORS WILL NOT BE RESPONSIBLE FOR ANY ILLEGAL USAGE.***


OWASP Nettacker project is created to automate information gathering, vulnerability scanning and eventually generating a report for networks, including services, bugs, vulnerabilities, misconfigurations, and other information. This software **will** utilize TCP SYN, ACK, ICMP and many other protocols in order to detect and bypass Firewall/IDS/IPS devices. By leveraging a unique method in OWASP Nettacker for discovering protected services and devices such as SCADA. It would make a competitive edge compared to other scanner making it one of the bests.


* OWASP Page: https://www.owasp.org/index.php/OWASP_Nettacker
* Home: http://nettacker.z3r0d4y.com/
* Github: https://github.com/viraintel/OWASP-Nettacker
* Mailing List: https://groups.google.com/forum/#!forum/owasp-nettacker
* Docker Image: https://hub.docker.com/r/alirazmjoo/owaspnettacker/


```



   ______          __      _____ _____
  / __ \ \        / /\    / ____|  __ \
 | |  | \ \  /\  / /  \  | (___ | |__) |
 | |  | |\ \/  \/ / /\ \  \___ \|  ___/
 | |__| | \  /\  / ____ \ ____) | |     Version 0.0.1
  \____/   \/  \/_/    \_\_____/|_|     SAME
                          _   _      _   _             _
                         | \ | |    | | | |           | |
  github.com/viraintel   |  \| | ___| |_| |_ __ _  ___| | _____ _ __
  owasp.org              | . ` |/ _ \ __| __/ _` |/ __| |/ / _ \ '__|
  viraintel.com          | |\  |  __/ |_| || (_| | (__|   <  __/ |
                         |_| \_|\___|\__|\__\__,_|\___|_|\_\___|_|



usage: Nettacker [-L LANGUAGE] [-v VERBOSE_LEVEL] [-V] [-c] [-o LOG_IN_FILE]
                 [--graph GRAPH_FLAG] [-h] [-i TARGETS] [-l TARGETS_LIST]
                 [-m SCAN_METHOD] [-x EXCLUDE_METHOD] [-u USERS]
                 [-U USERS_LIST] [-p PASSWDS] [-P PASSWDS_LIST] [-g PORTS]
                 [-T TIMEOUT_SEC] [-w TIME_SLEEP] [-r] [-s] [-t THREAD_NUMBER]
                 [-M THREAD_NUMBER_HOST] [-R PROXIES]
                 [--proxy-list PROXIES_FILE] [--retries RETRIES]
                 [--ping-before-scan] [--method-args METHODS_ARGS]
                 [--method-args-list]

Engine:
  Engine input options

  -L LANGUAGE, --language LANGUAGE
                        select a language ['ru', 'fr', 'en', 'nl', 'el', 'vi',
                        'id', 'de', 'tr', 'ps', 'ur', 'fa', 'hy', 'hi', 'ko',
                        'it', 'zh-cn', 'ar', 'ja', 'es']
  -v VERBOSE_LEVEL, --verbose VERBOSE_LEVEL
                        verbose mode level (0-5) (default 0)
  -V, --version         show software version
  -c, --update          check for update
  -o LOG_IN_FILE, --output LOG_IN_FILE
                        save all logs in file (results.txt, results.html)
  --graph GRAPH_FLAG    build a graph of all activities and information, you
                        must use HTML output. available graphs:
                        ['d3_tree_v1_graph', 'd3_tree_v2_graph',
                        'jit_circle_v1_graph']
  -h, --help            Show Nettacker Help Menu

Target:
  Target input options

  -i TARGETS, --targets TARGETS
                        target(s) list, separate with ","
  -l TARGETS_LIST, --targets-list TARGETS_LIST
                        read target(s) from file

Method:
  Scan method options

  -m SCAN_METHOD, --method SCAN_METHOD
                        choose scan method ['ftp_brute', 'smtp_brute',
                        'ssh_brute', 'dir_scan', 'port_scan',
                        'viewdns_reverse_ip_lookup_scan', 'all']
  -x EXCLUDE_METHOD, --exclude EXCLUDE_METHOD
                        choose scan method to exclude ['ftp_brute',
                        'smtp_brute', 'ssh_brute', 'dir_scan', 'port_scan',
                        'viewdns_reverse_ip_lookup_scan']
  -u USERS, --usernames USERS
                        username(s) list, separate with ","
  -U USERS_LIST, --users-list USERS_LIST
                        read username(s) from file
  -p PASSWDS, --passwords PASSWDS
                        password(s) list, separate with ","
  -P PASSWDS_LIST, --passwords-list PASSWDS_LIST
                        read password(s) from file
  -g PORTS, --ports PORTS
                        port(s) list, separate with ","
  -T TIMEOUT_SEC, --timeout TIMEOUT_SEC
                        read passwords(s) from file
  -w TIME_SLEEP, --time-sleep TIME_SLEEP
                        time to sleep between each request
  -r, --range           scan all IPs in the range
  -s, --sub-domains     find and scan subdomains
  -t THREAD_NUMBER, --thread-connection THREAD_NUMBER
                        thread numbers for connections to a host
  -M THREAD_NUMBER_HOST, --thread-hostscan THREAD_NUMBER_HOST
                        thread numbers for scan hosts
  -R PROXIES, --proxy PROXIES
                        proxy(s) list, separate with "," (out going
                        connections)
  --proxy-list PROXIES_FILE
                        read proxies from a file (outgoing connections)
  --retries RETRIES     Retries when the connection timeout (default 3)
  --ping-before-scan    ping before scan the host
  --method-args METHODS_ARGS
                        enter methods inputs, example: "ftp_brute_users=test,a
                        dmin&ftp_brute_passwds=read_from_file:/tmp/pass.txt&ft
                        p_brute_port=21"
  --method-args-list    list all methods args


Please read license and agreements https://github.com/viraintel/OWASP-Nettacker
```

* ***IoT Scanner***
*	Python Multi Thread & Multi Process Network Information Gathering Vulnerability Scanner
*	Service and Device Detection ( SCADA, Restricted Areas, Routers, HTTP Servers, Logins and Authentications, None-Indexed HTTP, Paradox System, Cameras, Firewalls, UTM, WebMails, VPN, RDP, SSH, FTP, TELNET Services, Proxy Servers and Many Devices like Juniper, Cisco, Switches and many more… ) 
*	Network Service Analysis
*	Services Brute Force Testing
*	Services Vulnerability Testing
*	HTTP/HTTPS Crawling, Fuzzing, Information Gathering and … 
*	HTML and Text Outputs
*	This project is at the moment in research and development phase and most of results/codes are not published yet.
