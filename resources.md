## Blacklist
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| PhishTank     | 4      | Yes        | Yes         | Yes | No          | No | WebUI/API| XML/CSV/JSON/Serialized PHP | phishing |
| OpenPhish     | 2      | No         | Yes         | Yes | No          | No            | WebUI/FILE    | XML/TXT     | phishing |
| CleanMXPhishing | 4    | Yes        | Yes         | Yes | No          | No            | WebUI/RSS/MAIL| XML/TXT     | phishing |
| SpamCop       | 3      | Yes        | Yes         | No  | No          | No            | WebUI         | XML         | spamming |
| CleanMXSpamming | 4    | Yes        | Yes         | Yes | No          | No            | WebUI/RSS/MAIL| XML/TXT     | spamming |
| CleanMXSpammingAccount | 4 | Yes    | Yes         | Yes | No          | No            | WebUI/RSS/MAIL| XML/TXT     | spamming |
| CleanMXVirus  | 4      | Yes        | Yes         | Yes | No          | No            | WebUI/RSS/MAIL| XML/TXT     | malware  |
| MalwareDomainList | 4  | Yes        | Yes         | Yes | No          | No            | WebUI/RSS     | XML         | malware  |
| DNS-BH        | 3      | Yes        | Yes         | No  | No          | No            | RSS/FILE      | XML/TXT     | malware  |
| MalwareURL    | 2      | Yes        | Yes         | No  | No          | No            | FILE          | TXT         | malware  |
| Malc0de       | 4      | Yes        | Yes         | Yes | No          | No            | WebUI/RSS/FILE| XML/TXT     | malware  |
| ZeusTracker   | 5      | Yes        | Yes         | Yes | Yes         | No            | WebUI/API/RSS/FILE | XML/TXT| malware  |
| FeodoTracker  | 2      | Yes        | No          | No  | No          | No            | WebUI/RSS/FILE| XML/TXT     | malware  |
| SSLBlacklist  | 2      | Yes        | No          | No  | No          | No            | WebUI/RSS/FILE| XML/TXT     | malware  |
| CyberCrimeTracker | 4  | Yes        | Yes         | Yes | No          | No            | WebUI/RSS/FILE| XML/TXT     | malware  |
| SCUMWARE      | 4      | Yes        | Yes         | Yes | No          | No            | WebUI         | XML         | malware  |
| Malware Patrol| 4      | Yes        | Yes         | Yes | No          | No            | WebUI/API     | XML/TXT     | malware  |
| CriticalStack Intel | 4| Yes        | Yes         | Yes | No          | No            | WebUI/API     | XML/Bro     | misc     |
| Bambenek Consulting | 4| Yes        | Yes         | Yes | No          | No            | FILE          | TXT         | malware  |
| EmergingThreats | 2    | Yes        | No          | No  | No          | No            | FILE          | TXT/Snort   | malware  |
| hpHosts       | 3      | Yes        | Yes         | No  | No          | No            | FILE          | TXT         | misc     |
| ProjectHoneyPot| 2     | Yes        | Yes         | No  | No          | No            | WebUI/RSS/FILE| XML/TXT     | misc     |
| FireHOLIPLists| 2      | Yes        | No          | No  | No          | No            | FILE          | TXT         | misc     |
| Spamhaus      | 4      | Yes        | Yes         | Yes | No          | No            | API           | System      | misc     |
| ShadowServer  | 5      | Yes        | Yes         | Yes | Yes         | No            | MAIL/API/     | CSV         | misc     |
| ThreatLog     | 2      | Yes        | Yes         | No  | No          | No            | WebUI         | XML         | misc     |
| URLBlacklist  | TBD    | TBD        | TBD         | TBD | TBD         | TBD           | TBD           | TBD         | TBD      |

* [PhishTank](https://www.phishtank.com/)
* [OpenPhish](https://openphish.com/)
* [Clean MX Phishing](http://support.clean-mx.de/clean-mx/phishing.php)
* [SpamCop](https://www.spamcop.net/)
* [Clean MX Spamming](http://support.clean-mx.com/clean-mx/portals.php)
* [Clean MX Spamming Account](http://support.clean-mx.de/clean-mx/publog.php)
* [Clean MX Virus](http://support.clean-mx.de/clean-mx/viruses.php)
* [Malware Domain List](https://www.malwaredomainlist.com/)
* [DNS-BH](http://www.malwaredomains.com/)
* [Malware URL](https://www.malwareurl.com/)
* [Malc0de](https://malc0de.com/database)
* [Zeus Tracker](https://zeustracker.abuse.ch/)
* [Feodo Tracker](https://feodotracker.abuse.ch)
* [SSL Blacklist](https://sslbl.abuse.ch/)
* [CyberCrime Tracker](http://cybercrime-tracker.net/)
* [SCUMWARE](http://www.scumware.org/)
* [Malware Patrol](http://www.malware.com.br/)
* [CriticalStack Intel](https://intel.criticalstack.com/)
* [BambenekConsulting](http://osint.bambenekconsulting.com/feeds/)
* [Emerging Threats](http://rules.emergingthreats.net/)
* [Malwarebytes hpHosts](http://hosts-file.net/)
* [Project Honey Pot](https://www.projecthoneypot.org/)
* [FireHOL IP Lists](http://iplists.firehol.org/)
* [Spamhaus](http://www.spamhaus.org/)
* [The Shadowserver Foundation](https://www.shadowserver.org)
* [ThreatLog](http://www.threatlog.com/)
* [URLBlacklist](http://www.urlblacklist.com/)

## Whitelist
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| AlexaTop500   | 1      | No         | Yes         | No  | No          | No            | WebUI         | XML         | benign   |
| AlexaTop1M    | 1      | No         | Yes         | No  | No          | No            | FILE          | CSV         | benign   |
| DNSWL         | TBD    | TBD        | TBD         | TBD | TBD         | TBD           | TBD           | TBD         | TBD      |

* [Alexa Top 500 Web sites](http://www.alexa.com/topsites)
* [Alexa Top 1M Web sites](http://s3.amazonaws.com/alexa-static/top-1m.csv.zip)
* [DNSWL.org](http://www.dnswl.org)

## Specimen
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| Contagio      | 5      | Yes        | Yes         | Yes | Yes         | Yes           | RSS/FILE      | XML/BIN     | malware  |
| ContagioMobile| 5      | Yes        | Yes         | Yes | Yes         | No            | RSS/FILE      | XML/BIN     | malware  |
| Malekal's forum | 5    | Yes        | Yes         | Yes | Yes         | No            | WebUI/RSS/FILE| XML/BIN     | malware  |
| VXVault       | 5      | Yes        | Yes         | Yes | Yes         | No            | WebUI/RSS/FILE| XML/TXT/BIN | malware  |
| Malwerk       | 2      | No         | No          | No  | Yes         | No            | FILE          | BIN         | malware  |
| TheZoo        | 2      | No         | No          | No  | Yes         | No            | FILE          | BIN         | malware  |
| MalShare      | 5      | Yes        | Yes         | Yes | Yes         | No            | WebUI/API/FILE|XML/TXT/JSON/BIN|malware|
| VirusShare    | 2      | No         | No          | No  | Yes         | No            | WebUI/FILE    | TORRENT     | malware  |
| ViruSign      | 2      | No         | No          | No  | Yes         | TBD           | WebUI         | XML         | malware  |
| InsideYourBotnet | 5   | Yes        | Yes         | Yes | Yes         | No            | WebUI/RSS/FILE| XML/BIN     | malware  |
| NoThink Honeypots | 4  | Yes        | Yes         | No  | Yes         | No            | WebUI/FILE    | XML/JSON/BIN| malware  |
| VirusSign     | TBD    | TBD        | TBD         | TBD | TBD         | TBD           | TBD           | TBD         | TBD      |

* [Contagio](https://contagiodump.blogspot.com/)
* [Contagio Mobile](https://contagiominidump.blogspot.com/)
* [Malekal's forum](http://malwaredb.malekal.com/)
* [VXVault](http://vxvault.net/ViriList.php)
* [MALWERK](http://dasmalwerk.eu/)
* [The Zoo](https://ytisf.github.io/theZoo/)
* [MalShare](http://www.malshare.com/)
* [VirusShare](http://virusshare.com/)
* [ViruSign](http://www.virusign.com/)
* [Inside Your Botnet](http://www.exposedbotnets.com/)
* [NoThink Honeypots](http://www.nothink.org/honeypots.php)
* [VirusSign](http://www.virussign.com/)

## Network Trace
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| PANDA-Malrec  | 2      | No         | No          | No  | No          | Yes           | WebUI/FILE    | PCAP/RRLOG  | malware  |
| ContagioPcap  | 2      | No         | No          | No  | No          | Yes           | MediaFire     | ZIP/PCAP    | malware  |

* [PANDA-Malrec](http://panda.gtisc.gatech.edu/malrec/)
* [ContagioPcap](http://contagiodump.blogspot.com/2013/04/collection-of-pcap-files-from-malware.html)

## Online Anti-Virus/Sandbox/Lookup Service
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| urlQuery      | 4      | Yes        | Yes         | Yes | No          | No            | WebUI         | XML         | malware  |
| ThreatExpert  | 4      | Yes        | Yes         | No  | No          | No            | WebUI         | XML         | malware  |
| VirusTracker  | 4      | Yes        | Yes         | Yes | No          | No            | WebUI/FILE    | XML/CSV     | malware  |
| VirusTotal    | 5      | Yes        | Yes         | Yes | Yes         | No            | WebUI/API/FILE| XML/BIN     | malware  |
| GoogleSafeBrowsing | 4 | Yes        | Yes         | Yes | No          | No            | WebUI/API     | XML         | malware  |
| IBMX-ForceExchange | 4 | Yes        | Yes         | Yes | No          | No            | WebUI/API     | XML/JSON    | misc     |
| AlienVaultOTX | 4      | Yes        | Yes         | Yes | No          | No            | WebUI/API     | XML/JSON    | misc     |
| VxStreamSandbox| 5     | Yes        | Yes         | Yes | Yes         | Yes           | WebUI         | XML         | malware  |
| Malwr         | 5      | Yes        | Yes         | Yes | Yes         | No            | WebUI/API/FILE| XML/BIN     | malware  |
| Malware.lu    | 2      | No         | No          | No  | Yes         | No            | WebUI/API/FILE| XML/BIN     | malware  |
| DomainCrawler | 3      | Yes        | Yes         | No  | No          | No            | WebUI         | XML         | misc     |
| IPVoid        | 2      | Yes        | No          | No  | No          | No            | WebUI         | XML         | misc     |
| URLVoid       | 2      | Yes        | No          | No  | No          | No            | WebUI         | XML/API     | misc     |
| FBThreatExchange| TBD  | TBD        | TBD         | TBD | TBD         | TBD           | TXAII         | TBD         | TBD      |
| SANS-ISC      | 4      | Yes        | Yes         | No  | No          | No            | WebUI/FILE    | XML/TXT     | misc     |

* [urlQuery](https://urlquery.net/index.php)
* [Threat Expert](http://www.threatexpert.com/reports.aspx)
* [Virus Tracker](https://virustracker.net/)
* [Virus Total](https://www.virustotal.com/)
* [Google Safe Browsing](https://www.google.com/safebrowsing/diagnostic?site=Google.com)
* [IBM X-Force Exchange](https://exchange.xforce.ibmcloud.com/)
* [AlienVault Open Threat Exchange](https://otx.alienvault.com/)
* [VxStream Sandbox](https://www.hybrid-analysis.com/)
* [Malwr](https://malwr.com/)
* [Malware.lu](https://malware.lu/)
* [DomainCrawler](http://www.domaincrawler.com/)
* [IPVoid](http://www.ipvoid.com/)
* [URLVoid](http://www.urlvoid.com/)
* [Facebook ThreatExchange](https://developers.facebook.com/products/threat-exchange)
* [SANS - Internet Storm Center (dshield)](https://isc.sans.edu/)
* [Free Online Tools for Looking up Potentially Malicious Websites](https://zeltser.com/lookup-malicious-websites/)

## STIX & TAXII Threat Intelligence Repository
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| HailaTAXII    | TBD    | TBD        | TBD         | TBD | TBD         | TBD           | TXAII         | TBD         | TBD      |

* [Hail a TAXII](http://hailataxii.com/)

## Others
| Resource Name | Weight | IP Address | Domain Name | URL | Binary File | Network Trace | Access Method | Format      | Category |
|:------------- |:------ |:---------- |:----------- |:--- |:----------- |:------------- |:------------- |:----------- |:-------- |
| McAfeeSiteAdvisor | TBD| TBD        | TBD         | TBD | TBD         | TBD           | TBD           | TBD         | TBD      |
| name          | 12345  | Yes/No     | Yes/No      | Y/N | Yes/No      | Yes/No        | WebUI/API/RSS | XML/TXT     | misc     |

* [McAfee SiteAdvisor](https://www.siteadvisor.com/)
