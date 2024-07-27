# Домашнее задание к занятию "13-03 Защита сети" - Пергунов Дмитрий


### Задание 1

1. Установили и настроили Suricata и NMAP
<details>
  <summary>2. События, которые попали в логи Suricata</summary>

```
07/27/2024-09:50:47.359350  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35848 -> 192.168.0.7:1521
07/27/2024-09:50:47.355272  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:42666 -> 192.168.0.7:3306
07/27/2024-09:50:47.355272  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:42666 -> 192.168.0.7:3306
07/27/2024-09:50:47.359350  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35848 -> 192.168.0.7:1521
07/27/2024-09:50:47.391469  [**] [1:2002911:6] ET SCAN Potential VNC Scan 5900-5920 [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:45346 -> 192.168.0.7:5907
07/27/2024-09:50:47.398857  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:47980 -> 192.168.0.7:5432
07/27/2024-09:50:47.391469  [**] [1:2002911:6] ET SCAN Potential VNC Scan 5900-5920 [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:45346 -> 192.168.0.7:5907
07/27/2024-09:50:47.398857  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:47980 -> 192.168.0.7:5432
07/27/2024-09:50:47.452520  [**] [1:2002910:6] ET SCAN Potential VNC Scan 5800-5820 [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:49856 -> 192.168.0.7:5815
07/27/2024-09:50:47.452520  [**] [1:2002910:6] ET SCAN Potential VNC Scan 5800-5820 [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:49856 -> 192.168.0.7:5815
07/27/2024-09:50:47.473929  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:40920 -> 192.168.0.7:1433
07/27/2024-09:50:47.473929  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:40920 -> 192.168.0.7:1433
07/27/2024-09:50:54.366989  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:3306
07/27/2024-09:50:54.366989  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:3306
07/27/2024-09:50:54.420715  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:1521
07/27/2024-09:50:54.420715  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:1521
07/27/2024-09:50:54.584661  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:1433
07/27/2024-09:50:54.584661  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:1433
07/27/2024-09:50:54.716893  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:5432
07/27/2024-09:50:54.716893  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:35610 -> 192.168.0.7:5432
07/27/2024-09:51:03.798481  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:5432
07/27/2024-09:51:03.796487  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:3306
07/27/2024-09:51:03.798481  [**] [1:2010939:3] ET SCAN Suspicious inbound to PostgreSQL port 5432 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:5432
07/27/2024-09:51:03.796487  [**] [1:2010937:3] ET SCAN Suspicious inbound to mySQL port 3306 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:3306
07/27/2024-09:51:03.825329  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:1433
07/27/2024-09:51:03.825329  [**] [1:2010935:3] ET SCAN Suspicious inbound to MSSQL port 1433 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:1433
07/27/2024-09:51:03.899313  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:1521
07/27/2024-09:51:03.899313  [**] [1:2010936:3] ET SCAN Suspicious inbound to Oracle SQL port 1521 [**] [Classification: Potentially Bad Traffic] [Priority: 2] {TCP} 192.168.0.5:58746 -> 192.168.0.7:1521
```

</details>

<details>
  <summary>3. События, которые попали в логи Fail2ban</summary>

```
sudo cat /var/log/fail2ban.log
2024-07-27 09:33:52,616 fail2ban.server         [3561]: INFO    --------------------------------------------------
2024-07-27 09:33:52,616 fail2ban.server         [3561]: INFO    Starting Fail2ban v1.0.2
2024-07-27 09:33:52,617 fail2ban.observer       [3561]: INFO    Observer start...
2024-07-27 09:33:52,635 fail2ban.database       [3561]: INFO    Connected to fail2ban persistent database '/var/lib/fail2ban/fail2ban.sqlite3'
2024-07-27 09:33:52,638 fail2ban.database       [3561]: WARNING New database created. Version '4'
2024-07-27 09:33:52,638 fail2ban.jail           [3561]: INFO    Creating new jail 'sshd'
2024-07-27 09:33:53,513 fail2ban.jail           [3561]: INFO    Jail 'sshd' uses systemd {}
2024-07-27 09:33:53,514 fail2ban.jail           [3561]: INFO    Initiated 'systemd' backend
2024-07-27 09:33:53,514 fail2ban.filter         [3561]: INFO      maxLines: 1
2024-07-27 09:33:53,525 fail2ban.filtersystemd  [3561]: INFO    [sshd] Added journal match for: '_SYSTEMD_UNIT=sshd.service + _COMM=sshd'
2024-07-27 09:33:53,525 fail2ban.filter         [3561]: INFO      maxRetry: 5
2024-07-27 09:33:53,525 fail2ban.filter         [3561]: INFO      findtime: 600
2024-07-27 09:33:53,525 fail2ban.actions        [3561]: INFO      banTime: 600
2024-07-27 09:33:53,525 fail2ban.filter         [3561]: INFO      encoding: UTF-8
2024-07-27 09:33:53,527 fail2ban.jail           [3561]: INFO    Jail 'sshd' started
2024-07-27 09:33:53,828 fail2ban.filtersystemd  [3561]: INFO    [sshd] Jail is in operation now (process new journal entries)
2024-07-27 09:42:52,741 fail2ban.server         [3561]: INFO    Shutdown in progress...
2024-07-27 09:42:52,741 fail2ban.observer       [3561]: INFO    Observer stop ... try to end queue 5 seconds
2024-07-27 09:42:52,765 fail2ban.observer       [3561]: INFO    Observer stopped, 0 events remaining.
2024-07-27 09:42:52,804 fail2ban.server         [3561]: INFO    Stopping all jails
2024-07-27 09:42:53,881 fail2ban.actions        [3561]: NOTICE  [sshd] Flush ticket(s) with nftables
2024-07-27 09:42:53,881 fail2ban.jail           [3561]: INFO    Jail 'sshd' stopped
2024-07-27 09:42:53,883 fail2ban.database       [3561]: INFO    Connection to database closed.
2024-07-27 09:42:53,883 fail2ban.server         [3561]: INFO    Exiting Fail2ban
2024-07-27 09:43:31,084 fail2ban.server         [728]: INFO    --------------------------------------------------
2024-07-27 09:43:31,115 fail2ban.server         [728]: INFO    Starting Fail2ban v1.0.2
2024-07-27 09:43:31,116 fail2ban.observer       [728]: INFO    Observer start...
2024-07-27 09:43:31,433 fail2ban.database       [728]: INFO    Connected to fail2ban persistent database '/var/lib/fail2ban/fail2ban.sqlite3'
2024-07-27 09:43:31,434 fail2ban.jail           [728]: INFO    Creating new jail 'sshd'
2024-07-27 09:43:32,627 fail2ban.jail           [728]: INFO    Jail 'sshd' uses systemd {}
2024-07-27 09:43:32,628 fail2ban.jail           [728]: INFO    Initiated 'systemd' backend
2024-07-27 09:43:32,628 fail2ban.filter         [728]: INFO      maxLines: 1
2024-07-27 09:43:32,637 fail2ban.filtersystemd  [728]: INFO    [sshd] Added journal match for: '_SYSTEMD_UNIT=sshd.service + _COMM=sshd'
2024-07-27 09:43:32,637 fail2ban.filter         [728]: INFO      maxRetry: 5
2024-07-27 09:43:32,637 fail2ban.filter         [728]: INFO      findtime: 600
2024-07-27 09:43:32,637 fail2ban.actions        [728]: INFO      banTime: 600
2024-07-27 09:43:32,637 fail2ban.filter         [728]: INFO      encoding: UTF-8
2024-07-27 09:43:32,657 fail2ban.jail           [728]: INFO    Jail 'sshd' started
2024-07-27 09:43:33,058 fail2ban.filtersystemd  [728]: INFO    [sshd] Jail is in operation now (process new journal entries)
```

</details>
4. Suricata записала в журнал все события, связанные со сканированием портов другой машиной в сети, включая детали о сканируемых портах и целях сканирования.   

В логах fail2ban ничего не зафиксировано, так как подбор пароля не осуществлялся, а проводилось только сканирование портов на доступность.  

### Задание 2

<details>
  <summary>1. Запустили подбор паролей с помощью Hydra и попали в ban лист </summary>

```
hydra -L users.txt -P passwords.txt 192.168.0.7 ssh
Hydra v9.4 (c) 2022 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2024-07-27 15:14:20
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore
[DATA] max 16 tasks per 1 server, overall 16 tasks, 9612 login tries (l:108/p:89), ~601 tries per task
[DATA] attacking ssh://192.168.0.7:22/
[ERROR] could not connect to ssh://192.168.0.7:22 - Connection refused
```

</details>

<details>
  <summary>2. Лог Fail2ban </summary>

   ```
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:13:58,505 fail2ban.actions        [1519]: WARNING [sshd] 192.168.0.5 already banned
2024-07-27 10:14:02,931 fail2ban.server         [1519]: INFO    Shutdown in progress...
2024-07-27 10:14:02,931 fail2ban.observer       [1519]: INFO    Observer stop ... try to end queue 5 seconds
2024-07-27 10:14:02,952 fail2ban.observer       [1519]: INFO    Observer stopped, 0 events remaining.
2024-07-27 10:14:02,994 fail2ban.server         [1519]: INFO    Stopping all jails
2024-07-27 10:14:03,113 fail2ban.actions        [1519]: NOTICE  [sshd] Flush ticket(s) with nftables
2024-07-27 10:14:03,127 fail2ban.actions        [1519]: NOTICE  [sshd] Unban 192.168.0.5
2024-07-27 10:14:03,191 fail2ban.jail           [1519]: INFO    Jail 'sshd' stopped
2024-07-27 10:14:03,192 fail2ban.database       [1519]: INFO    Connection to database closed.
2024-07-27 10:14:03,192 fail2ban.server         [1519]: INFO    Exiting Fail2ban
2024-07-27 10:14:03,313 fail2ban.server         [1561]: INFO    --------------------------------------------------
2024-07-27 10:14:03,314 fail2ban.server         [1561]: INFO    Starting Fail2ban v1.0.2
2024-07-27 10:14:03,314 fail2ban.observer       [1561]: INFO    Observer start...
2024-07-27 10:14:03,319 fail2ban.database       [1561]: INFO    Connected to fail2ban persistent database '/var/lib/fail2ban/fail2ban.sqlite3'
2024-07-27 10:14:03,319 fail2ban.jail           [1561]: INFO    Creating new jail 'sshd'
2024-07-27 10:14:03,398 fail2ban.jail           [1561]: INFO    Jail 'sshd' uses systemd {}
2024-07-27 10:14:03,398 fail2ban.jail           [1561]: INFO    Initiated 'systemd' backend
2024-07-27 10:14:03,399 fail2ban.filter         [1561]: INFO      maxLines: 1
2024-07-27 10:14:03,409 fail2ban.filtersystemd  [1561]: INFO    [sshd] Added journal match for: '_SYSTEMD_UNIT=sshd.service + _COMM=sshd'
2024-07-27 10:14:03,409 fail2ban.filter         [1561]: INFO      maxRetry: 5
2024-07-27 10:14:03,409 fail2ban.filter         [1561]: INFO      findtime: 600
2024-07-27 10:14:03,409 fail2ban.actions        [1561]: INFO      banTime: 600
2024-07-27 10:14:03,409 fail2ban.filter         [1561]: INFO      encoding: UTF-8
2024-07-27 10:14:03,411 fail2ban.filtersystemd  [1561]: INFO    [sshd] Jail is in operation now (process new journal entries)
2024-07-27 10:14:03,415 fail2ban.jail           [1561]: INFO    Jail 'sshd' started
2024-07-27 10:14:03,611 fail2ban.actions        [1561]: NOTICE  [sshd] Restore Ban 192.168.0.5

   ```

</details>

<details>
  <summary>3. Лог Surricata </summary>

```
07/27/2024-10:11:16.136143  [**] [1:2003068:7] ET SCAN Potential SSH Scan OUTBOUND [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:34070 -> 192.168.0.7:22
07/27/2024-10:11:16.140663  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.7:22 -> 192.168.0.5:34078
07/27/2024-10:11:16.149012  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.7:22 -> 192.168.0.5:34092
07/27/2024-10:11:16.155818  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.7:22 -> 192.168.0.5:34106
07/27/2024-10:11:16.156566  [**] [1:2006546:9] ET SCAN LibSSH Based Frequent SSH Connections Likely BruteForce Attack [**] [Classification: Attempted Administrator Privilege Gain] [Priority: 1] {TCP} 192.168.0.5:34106 -> 192.168.0.7:22
07/27/2024-10:11:16.171630  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.7:22 -> 192.168.0.5:34136
07/27/2024-10:11:16.179331  [**] [1:2003068:7] ET SCAN Potential SSH Scan OUTBOUND [**] [Classification: Attempted Information Leak] [Priority: 2] {TCP} 192.168.0.5:34146 -> 192.168.0.7:22
07/27/2024-10:11:16.182687  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.7:22 -> 192.168.0.5:34146
07/27/2024-10:12:23.574659  [**] [1:2260002:1] SURICATA Applayer Detect protocol only one direction [**] [Classification: Generic Protocol Command Decode] [Priority: 3] {TCP} 192.168.0.5:34156 -> 192.168.0.7:22

```

</details>
4. Как мы видим из логов Fail2ban посторонний хост пытался подбирать пароль и был забанен.  
Из логов Surricata видно, то что осуществлялся подбор пароля на порту 22 SSH



