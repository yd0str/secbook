Malicious DNS and Infected Host Detection Features
==================================================
@(Research Notebook)[malware, dns, machine learning, network, blacklist, whitelist]

----

[TOC]

----

### Temporal Features

Table 1: Temporal Features

| Feature                                | \#.| Source               | Comment |
| :------------------------------------- | :-:| :------------------- | :------ |
| Daily Similarity                       |  1 | [scholarly paper][1] |         |
| Same Query Numbers in Same Time Window |  2 | [scholarly paper][1] |         |
| Very Low Frequency Query               |  3 | [scholarly paper][1] |         |
| Average TTL                            |  4 | [scholarly paper][1] |         |

#### Daily Similarity
- Check if the domains have daily similarities in changing IP address at the same intervals everyday.
- 藉由特定區間的次數統計，用以偵測駭客操控改變 Domain 對應 IP的變化。
- 範例1: 某些 APT攻擊的情境中，駭客則會在上工時才將Domain指向有效的伺服器IP，結束後就將其指向內部或無效IP。

#### Same Query Numbers in Same Time Window
- In the same time window, the number of domain queries are about the same. The infected host will mistaken DNS errors and send large amounts of repeated DNS queries. (NXDomain)
- 藉由特定區間的次數統計，用以偵測受害電腦查詢 Domain 的固定頻率。
- 範例1: 有一些惡意程式，會在沒有接獲指令情形下固定每日報到特定 C&C 伺服器數次。

#### Very Low Frequency Query
- A few high advanced APT malware query domains to locate command and control server at very low frequency, at one time for serval days or even serval weeks.
- The resolving IP address and Time To Live (TTL) of the domain name are all stable.
- 某些 APT惡意程式會有非常低的查詢頻率
- 可能特徵: 連線目的 Domain指向的皆為Web Server，且具有相同固定內容（空白頁與under construction？）。

#### Average TTL
- Setting TTL values of host names to lower values can help the attacker to change the C&C server rapidly. Moreover, based on our measurements, TTL values of Dynamic Domain Name Service, such as DynDNS, NO-IP and ChangeIP, are usually set to 30, 31, 60, 300 seconds.
- 通常設置低值的TTL可以讓駭客快速改變C&C的IP，但這部分通常用在Malware/Botnet上，有些則反其道而行設定非常長的TTL區間。


### Spatial Features

Table 2: Spatial Features

| Feature                                | \#.| Source               | Comment |
| :------------------------------------- | :-:| :------------------- | :------ |
| Number of Distinct IP Addresses        |  1 | [scholarly paper][1] |         |
| Number of Distinct Countries           |  2 | [scholarly paper][1] |         |
| IP in the same Class B range of known C&C servers |3| [scholarly paper][1] | |

#### Number of Distinct IP Addresses
- Attackers usually use servers reside in different countries or regions they control or manage as C&C servers.
- 通常駭客會將惡意Domain指向的C&C  IP變動，並一直在各個國家轉換，以避免被追緝

#### Number of Distinct Countries
- Attackers usually use servers reside in different countries or regions they control or manage as C&C servers.
- 通常駭客會將惡意Domain指向的C&C  IP變動，並一直在各個國家轉換，以避免被追緝

#### IP in the same Class B range of known C&C servers
- There are many C&C servers in the same Class B IP addresses range and even in the same Class A range.
- There are more and more APT attackers rent VPS servers as C&C servers. Because VPS server is stable, hard to trace back and easy to manage.
- Some advanced attackers constructed special network for C&C servers.
- 範例: 駭客會租用 VPS伺服器或是 特定的網路傳輸網段來作為C&C伺服器服務


### Literal Features

Table 3: Literal Features

| Feature                 | \#.| Source               | Comment |
| :---------------------- | :-:| :------------------- | :------ |
| Contain Famous Name     |  1 | [scholarly paper][1] |         |
| Contain Particular Name |  2 | [scholarly paper][1] |         |
| Contain Phishing Name   |  3 | [scholarly paper][1] |         |

#### Contain Famous Name
- Famous domain names such as windows, yahoo and taobao
- 用以偵測含有合法公司名稱之 Domain，亦即偽冒成正常公司的 Domain。

#### Contain Particular Name
- Contain some particular name, such as "web", "mail", "news" and "update"
- 用以偵測含有合法服務名稱之  Domain，亦即偽冒成正常服務的 Domain。
- 範例："yahoomail.xxx.com", "yahoonews.xxx.com" and "windowsupdate.xxx.com"

#### Contain Phishing Name
- Phishing domain has a similar name to a legitimate one.
- 用以偵測類似於合法公司或服務名稱之 Domain，使用障眼法特定符號來取代部分字元。
- 範例："youtuhe.com" compared to "youtube.com", "yah00.com" compared to "yahoo.com", etc.


### Behavioral Features

Table 4: Behavioral Features

| Feature                       | \#.| Source               | Comment |
| :---------------------------- | :-:| :------------------- | :------ |
| Silent IP                     |  1 | [scholarly paper][1] |         |
| Predefined IP                 |  2 | [scholarly paper][1] |         |
| Number of Domains Share the Same IP with |3| [scholarly paper][1] | |

#### Silent IP
- To hide the C&C server and C&C network traffic, when attackers do not need to send commands to a victim machine, they do not want the domain names to point to the C&C server.
- 當連線閒置時，駭客不會把域名指向特定的IP，而是會讓 Domain呈現 IDLE狀態，通常是指向 127.0.0.1、192.168.x.x、172.16.x.x, 10.x.x.x、x.x.x.255 (broadcast address)等

#### Predefined IP
- When the domain is resolved to the predefined IP, the malware would turn to silent-mode and would not initiate a connection until the domain is resolved to another IP address.
- Predefined IP addresses are usually some invalid IP addresses that have obvious features, such as 5.5.5.5, 2.3.3.2.
- 某些特定的APT惡意程式會以C&C目前的指向IP來判別自己要接收或是執行什麼指令

#### Number of Domains Share the Same IP with
- In the APT attack scenario, a single attacker seldom own more than 30 dynamic names to locate command and control server in the same time, because it is not necessary and it is hard to maintain them.
- 因為物以類聚原則，Malware/Botnet駭客可能使用大量 Domain來設定與轉移C&C，但是對於APT駭客來說則不會，而是使用少量特定的C&C Domain，因此這是兩種惡意威脅的分界點。


### Blacklisted Features

Table 5: Behavioral Features


| Feature                 | Source               | Comment |
| :---------------------- | :------------------- | :------ |
| TBD                     | TBD                  | TBD     |


### Whitelisted Features

Table 6: Behavioral Features

| Feature                 | Source               | Comment |
| :---------------------- | :------------------- | :------ |
| TBD                     | TBD                  | TBD     |


### Active Probe Features

Table 7: Active Probe Features

| Feature                 | Source               | Comment |
| :---------------------- | :------------------- | :------ |
| Web Server or Not       | [scholarly paper][1] |         |
| Whois Information       | [scholarly paper][1] |         |

#### Web Server or Not
- Probe domain’s 80 port and check it is a true web server or not. If a domain keep TCP port 80 open but not a web server, it is highly suspicious.
- 若是某個 Domain解析指向的伺服器有80 Port，但是它卻沒有網頁服務，則很有可能是APT或是惡意的

####  Whois Information
- By querying Whois, we can get more information of the domain name, such as : the registration date, the registrar, the registrant name, the registrant email and the registered country.
- Comparing these information with the whois information of previous known malware C&C domains is an effective method.
- 從特定的註冊資訊來判別是否有可能是APT


----

[1]: http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=7163279
