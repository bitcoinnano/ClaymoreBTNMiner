Claymore's Bitcoin Nano AMD GPU Miner

Download Windows BTN AMD Miner

Download Linux BTN AMD Miner

=========================

Latest version v12.6 - BTG

Added support for BTG
Latest version v12.6:

added Vega cards support (ASM mode).
added ASM mode for RX460/560 cards (+20% speed).
new GPU sorting method for AMD cards. Now GPUs are sorted by physical bus index (it matches AfterBurner list of GPUs). Also the list of temperatures/fans matches the list of GPUs automatically. Therefore "-di detect" and "-gmap" options are not necessary and not supported anymore. WARNING: be careful if you use use separate overclock/temperature settings for every card, due to new sorting method GPUs can get different indexes!
added fan/OC support for 17.7.2 (and higher) drivers.
improved support for systems with more than 10 GPUs, check readme for "-di" option description for details.
added pool selection in runtime ("e" key).
a few minor improvements.
Latest version v12.5:

added support for latest ZCash forks.
improved fans management for latest drivers and Polaris cards.
added "-mpsw" option.
added shares-per-GPU statistics when "s" key is pressed.
Included EthMan v3.0 which supports passwords and email notifications.
Latest version v12.4:

slightly improved speed for some cards (1-2%).
added "-gmap" option.
a few minor changes/improvements.
Latest version v12.3:

slightly improved speed, about 410H/s on stock 390X, 465H/s on stock Nano, 300H/s on stock 280X, 305H/s on stock RX480.
improved stability for high "-i" option values, added "-i 9" option value.
fixed a few bugs.
Latest version v12.2:

fixed issue with "-ttli" option.
improved "-mport" option, now you can specify network adapter IP for incoming connections for remote management.
added "-old 1" option, try to use it if v12.0 works stable for you, but v12.1 is unstable.
Latest version v12.1:

slightly improved speed for some cards, about 410H/s on stock 390X, 450H/s on stock Nano, 290H/s on stock 280X, 300H/s on stock RX480.
slightly improved stability. If it is still unstable for you, reduce "-i" value.
fixed issue with wrong hashrate when "-li" or "-ttli" options enabled.
Latest version v12.0:

improved speed, about 405H/s on stock 390X, 450H/s on stock Nano, 290H/s on stock 280X, 295H/s on stock RX480.
Latest version v11.1:

improved speed, about 365H/s on stock 390X, 385H/s on stock Nano, 260H/s on stock 280X, 260H/s on stock RX480.
improved compatibility.
some bug fixes and minor improvements.
NOTES:

It seems there is no way to get full speed on latest drivers for Fiji and Polaris cards, at least in Windows. So don't use latest drivers for Fury, use 15.12 or 16.3.2. Since old drivers don't support Polaris, there is no way to get full speed for these cards at all, at least in Windows.
Tonga - currently I cannot get enough speedup from assembler for this card so I did not include assembler kernel for this card.
Latest version v11.0:

improved speed for Hawaii, Fury, Tahiti and Pitcairn cards. About 355H/s on stock 390X, 370H/s on stock Nano, 250H/s on stock 280X.
added faster assembler implementation kernels for these cards.
added "-asm" option.
Latest version v10.0:

improved speed for most cards, up to 8% (depends on card model). About 340H/s on stock 390X, 255H/s on stock RX480, 320H/x on stock Nano.
added "-a" option to select best algorithm implementation for your GPU.
Latest version v9.3:

improved stability and compatibility with various drivers.
slightly improved mining speed for some cards (1-2%). About 340H/s on stock 390X.
fixed issue in Linux version with GPU SEGFAULT and high CPU load.
added support for round robin DNS.
some bug fixes and minor improvements.
Latest version v9.2:

improved speed for some cards up to 7% (depends on card model). About 330H/s on stock 390X, 235H/s on stock RX480, 300H/x on stock Nano.
several bug fixes and minor improvements.
Latest version v9.1:

additional range checks in code for better stability.
reduced devfee, it's 2% now (72sec instead of 90sec) if you use secure SSL/TLS connection, currently Flypool and Suprnova pools support encrypted connections, see Readme for samples.
improved "-di detect" option: now after GPU order detection miner starts mining with the detected order.
added ability to use environment variables in "epools.txt" and "config.txt" files. For example, define "WORKER" environment varibale and use it as "%WORKER%" in config.txt.
Latest version v9.0:

improved speed by 3-20% (depends on card model). About 310H/s on stock 390X, 220H/s on stock RX480, 295H/x on stock Nano.
added "-i 7" and "-i 8" values, about 1% speedup, but can be unstable in some cases.
added SSL/TLS encryption support for better security, see "-zpool" option description in Readme file for details.
added "License.txt" file that contains the License Agreement.
added "-v" option.
several bug fixes and minor improvements.
EthMan: improved saving options.
Latest version v8.0:

improved speed by about 15-25% (depends on card model). Up to 300H/s on stock 390X.
added "-i 5" and "-i 6" values, 1-2% speedup, but can be unstable in some cases.
now remote management is working in read-only mode by default.
some bug fixes and minor improvements.
Latest version v7.0:

improved speed by about 15-25% (depends on card model). About 230H/s on stock 390X.
added "-benchmark" option.
Latest version v6.0:

improved speed by about 20-25% (depends on card model). About 180H/s on stock 390.
"-i" parameter values are 0...4 now, default value is "-i 4".
fixed issue with mixed cards.
Latest version v5.0:

improved speed by about 30-50% (depends on card model). About 145H/s on stock 390X.
improved support for Catalyst 16.x and 4xx cards.
reduced CPU usage.
Latest version v4.0:

improved speed by about 20% (depends on card model). Up to 100H/s on stock 390X on "-i 2" mode.
added "-retrydelay" option.
added "-nofee" option.
various bug fixes.
changed coloring.
EthMan: added "View miner console" command.
Latest version v3.0-3.1:

improved speed by 20-30% (depends on card model). Up to 80H/s on stock 390X on "-i 2" mode.
improved stability (3.1).
This version is for pools.

Catalyst (Crimson) 15.12 is required for best performance and compatibility. You can get very bad results for different drivers version, or miner can fail on startup. Set the following environment variables, especially if you have 2GB cards:

GPU_FORCE_64BIT_PTR 0 GPU_MAX_HEAP_SIZE 100 GPU_USE_SYNC_OBJECTS 1 GPU_MAX_ALLOC_PERCENT 100 GPU_SINGLE_ALLOC_PERCENT 100

For multi-GPU systems, set Virtual Memory size in Windows at least 16 GB: "Computer Properties / Advanced System Settings / Performance / Advanced / Virtual Memory".

This miner is free-to-use, however, current developer fee is 2.5%, every hour the miner mines for 90 seconds for developer. If you don't agree with the dev fee - don't use this miner.

This version is for recent AMD videocards only: 7xxx, 2xx, 3xx and 4xx, 2GB or more.

There are builds for Windows x64 and for Linux x64 (tested on Ubuntu 12.04). No 32-bit support. No NVidia support.

COMMAND LINE OPTIONS:

-zpool ZCash pool address. Only Stratum protocol is supported.

-zwal Your ZCash wallet address. Also worker name and other options if pool supports it. Pools that require "Login.Worker" instead of wallet address are not supported directly currently, but you can use "-allpools 1" option to mine there.

-zpsw Password for ZCash pool, use "x" as password.

-i mining intensity. Possible values: 0, 1, 2. 0 - lowest intensity and CPU usage, 2 - maximal intensity. You can also specify values for every card, for example "-i 0,2,1".

-allpools Specify "-allpools 1" if miner does not want to mine on specified pool (because it cannot mine devfee on that pool), but you agree to use some default pools for devfee mining. Note that if devfee mining pools will stop, entire mining will be stopped too.

-di GPU indexes, default is all available GPUs. For example, if you have four GPUs "-di 02" will enable only first and third GPUs (#0 and #2). Use "-di detect" value to detect correct GPU order for temperatures management (requires non-zero "-tt" option); note that it will not work properly if you do not want to assign all GPUs to miner. You can also turn on/off cards in runtime with "0"..."9" keys and check current statistics with "s" key.

-ftime failover main pool switch time, in minutes, see "Failover" section below. Default value is 30 minutes, set zero if there is no main pool.

-wd watchdog option. Default value is "-wd 1", it enables watchdog, miner will be closed (or restarted, see "-r" option) if any thread is not responding for 1 minute or OpenCL call failed. Specify "-wd 0" to disable watchdog.

-r Restart miner mode. "-r 0" (default) - restart miner if something wrong with GPU. "-r -1" - disable automatic restarting. -r >20 - restart miner if something wrong with GPU or by timer. For example, "-r 60" - restart miner every hour or when some GPU failed. "-r 1" closes miner and execute "reboot.bat" file ("reboot.bash" or "reboot.sh" for Linux version) in the miner directory (if exists) if some GPU failed. So you can create "reboot.bat" file and perform some actions, for example, reboot system if you put this line there: "shutdown /r /t 5 /f".

-retrydelay delay, in seconds, between connection attempts. Default values is "20". Specify "-retrydelay -1" if you don't need reconnection, in this mode miner will exit if connection is lost.

-dbg debug log and messages. "-dbg 0" - (default) create log file but don't show debug messages. "-dbg 1" - create log file and show debug messages. "-dbg -1" - no log file and no debug messages.

-logfile debug log file name. After restart, miner will append new log data to the same file. If you want to clear old log data, file name must contain "noappend" string. If missed, default file name will be used.

-nofee: set "1" to cancel my developer fee at all. In this mode some recent optimizations are disabled so mining speed will be slower by about 5%. By enabling this mode, I will lose 100% of my earnings, you will lose only 2.5% of your earnings. So you have a choice: "fastest miner" or "completely free miner but a bit slower". If you want both "fastest" and "completely free" you should find some other miner that meets your requirements, just don't use this miner instead of claiming that I need to cancel/reduce developer fee, saying that 2.5% developer fee is too much for this miner and so on.

-li low intensity mode. Reduces mining intensity, useful if your cards are overheated. Note that mining speed is reduced too. More value means less heat and mining speed, for example, "-li 10" is less heat and mining speed than "-li 1". You can also specify values for every card, for example "-li 3,10,50". Default value is "0" - no low intensity mode.

-tt set target GPU temperature. For example, "-tt 80" means 80C temperature. You can also specify values for every card, for example "-tt 70,80,75". You can also set static fan speed if you specify negative values, for example "-tt -50" sets 50% fan speed. Specify zero to disable control and hide GPU statistics. "-tt 1" (default) does not manage fans but shows GPU temperature and fan status every 30 seconds. Specify values 2..5 if it is too often. Note: for Linux gpu-pro drivers, miner must have root access to manage fans, otherwise only monitoring will be available.

-ttli reduce entire mining intensity (for all coins) automatically if GPU temperature is above specified value. For example, "-ttli 80" reduces mining intensity if GPU temperature is above 80C. You can see if intensity was reduced in detailed statistics ("s" key). You can also specify values for every card, for example "-ttli 80,85,80". You also should specify non-zero value for "-tt" option to enable this option. It is a good idea to set "-ttli" value higher than "-tt" value by 3-5C. NOTE: Check "KNOWN ISSUES" section. GPU indexes in temperature control sometimes don't match GPU indexes in mining!

-tstop set stop GPU temperature, miner will stop mining if GPU reaches specified temperature. For example, "-tstop 95" means 95C temperature. You can also specify values for every card, for example "-tstop 95,85,90". This feature is disabled by default ("-tstop 0"). You also should specify non-zero value for "-tt" option to enable this option. NOTE: Check "KNOWN ISSUES" section. GPU indexes in temperature control sometimes don't match GPU indexes in mining! If it turned off wrong card, it will close miner in 30 seconds. You can also specify negative value to close miner immediately instead of stopping GPU, for example, "-tstop -95" will close miner as soon as any GPU reach 95C temperature.

-fanmax set maximal fan speed, in percents, for example, "-fanmax 80" will set maximal fans speed to 80%. You can also specify values for every card, for example "-fanmax 50,60,70". This option works only if miner manages cooling, i.e. when "-tt" option is used to specify target temperature. Default value is "100".

-fanmin set minimal fan speed, in percents, for example, "-fanmin 50" will set minimal fans speed to 50%. You can also specify values for every card, for example "-fanmin 50,60,70". This option works only if miner manages cooling, i.e. when "-tt" option is used to specify target temperature. Default value is "0".

-cclock set target GPU core clock speed, in MHz. If not specified or zero, miner will not change current clock speed. You can also specify values for every card, for example "-cclock 1000,1050,1100,0". Unfortunately, AMD blocked underclocking for some reason, you can overclock only.

-mclock set target GPU memory clock speed, in MHz. If not specified or zero, miner will not change current clock speed. You can also specify values for every card, for example "-mclock 1200,1250,1200,0". Unfortunately, AMD blocked underclocking for some reason, you can overclock only.

-powlim set power limit, from -50 to 50. If not specified, miner will not change power limit. You can also specify values for every card, for example "-powlim 20,-20,0,10".

-cvddc set target GPU core voltage, multiplied by 1000. For example, "-cvddc 1050" means 1.05V. You can also specify values for every card, for example "-cvddc 900,950,1000,970". Supports latest AMD 4xx cards only in Windows.

-mvddc set target GPU memory voltage, multiplied by 1000. For example, "-mvddc 1050" means 1.05V. You can also specify values for every card, for example "-mvddc 900,950,1000,970". Supports latest AMD 4xx cards only in Windows.

-mport remote monitoring/management port. Default port is 3333, specify "-mport 0" to disable remote monitoring/management feature. Specify negative value to enable monitoring (get statistics) but disable management (restart, uploading files), for example, "-mport -3333" enables port 3333 for remote monitoring, but remote management will be blocked. You can also use your web browser to see current miner state, for example, type "localhost:3333" in web browser.

-colors enables or disables colored text in console. Default value is "1", use "-colors 0" to disable coloring.

CONFIGURATION FILE

You can use "config.txt" file instead of specifying options in command line. If there are not any command line options, miner will check "config.txt" file for options. If there is only one option in the command line, it must be configuration file name. If there are two or more options in the command line, miner will take all options from the command line, not from configuration file. Place one option per line, if first character of a line is ";" or "#", this line will be ignored.

SAMPLE USAGE

ZecMiner64.exe -zpool eu.pool.gold:3044 -zwal YOUR_WALLET_ADDRESS.YOUR_WORKER_NAME/YOUR_EMAIL -zpsw x

FAILOVER

Use "epools.txt" file to specify additional pools. This file has text format, one pool per line. Every pool has 3 connection attempts. Miner disconnects automatically if pool does not send new jobs for a long time or if pool rejects too many shares. If the first character of a line is ";" or "#", this line will be ignored. Do not change spacing, spaces between parameters and values are required for parsing. If you need to specify "," character in parameter value, use two commas - ,, will be treated as one comma. You can reload "epools.txt" file in runtime by pressing "r" key. Pool specified in the command line is "main" pool, miner will try to return to it every 30 minutes if it has to use some different pool from the list. If no pool was specified in the command line then first pool in the failover pools list is main pool. You can change 30 minutes time period to some different value with "-ftime" option, or use "-ftime 0" to disable switching to main pool.

REMOTE MONITORING/MANAGEMENT

Miner supports remote monitoring/management via JSON protocol over TCP/IP sockets, HTTP is supported as well. Start "EthMan.exe" from "Remote management" subfolder (Windows version only). Check "Help" tab for built-in help.

KNOWN ISSUES

AMD cards: GPU indexes in temperature control sometimes don't match GPU indexes in mining. Miner has to enumerate GPUs via OpenCL API to execute OpenCL code, and also it has to enumerate GPUs via ADL API to manage temperature/clock. And order of GPUs in these lists can be different. There is no way to fix GPUs order automatically, thanks to AMD devs. But you can do it manually. For example, if you have two cards, you can change their order by adding "-di 10". Another example, reverse order for six cards: "-di 543210". Also you can do it automatically (experimental feature) with "-di detect" option.
Windows 10 Defender recognizes miner as a virus, some antiviruses do the same. Miner is not a virus, add it to Defender exceptions. I write miners since 2014. Most of them are recognized as viruses by some paranoid antiviruses, perhaps because I pack my miners to protect them from disassembling, perhaps because some people include them into their botnets, or perhaps these antiviruses are not good, I don't know. For these years, a lot of people used my miners and nobody confirmed that my miner stole anything or did something bad. Note that I can guarantee clean binaries only for official links in my posts on this forum (bitcointalk). If you downloaded miner from some other link - it really can be a virus. However, my miners are closed-source so I cannot prove that they are not viruses. If you think that I write viruses instead of good miners - do not use this miner, or at least use it on systems without any valuable data.
TROUBLESHOOTING

Install Catalyst v15.12 (for AMD cards).
Disable overclocking.
Set environment variables as described above.
Set Virtual Memory 16 GB.
Reboot computer.
Check hardware, risers.
Set some timeout in .bat file before starting miner at system startup (30sec or even a minute), and try "-ethi 4" to check if it is more stable. It can help if miner is not stable on some system.
