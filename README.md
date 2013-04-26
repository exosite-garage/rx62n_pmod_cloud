rx62n_pmod_cloud
================

Using PMOD and RX62NRDK with Exosit cloud


This project is an example HEW project demonstrating how to use the Renesas
RX62N RDK with PMOD to send and receive data to/from the cloud by using 
Exosite's Cloud Data Platform.  The project is based on the Renesas toolchain's 
UIP networking stack example application.  The communication with the cloud is 
accomplished over HTTP in a RESTful style interface.  The project functionality 
writes the ping value to the cloud and reads data sources from the cloud and 
set value to the PMOD.  This project can be re-used, extended and deployed as desired.

PMODAD4 write value to alias 'adc1'.
PMODDA3 write ping value to alias 'ping' and read 'daout2' value then set it to PMOD.
PMODPOT write ping value to alias 'ping' and read 'dpout' value and set it to PMOD.

License is BSD, Copyright 2012, Exosite LLC (see LICENSE file)

Tested with HEW version 4.09.00.007, including:
High-performance Embedded Workshop 4.08.00	(2-17-2012 10:11:47)
C/C++ compiler package for RX family V.1.02 Release 00	(2-17-2012 12:33:40)

========================================
Quick Start
========================================
1) Install HEW, the RX toolchain 
* HINT: packages can be downloaded from Renesas at http://tinyurl.com/42turtk

2) Open the rx62n_rdk_cloud2.hws project workspace with HEW
* NOTE: The file "user_app.c" is the primary user app - modify to suit

3) Edit the "RECOVERYCIK" value in user_app.c to match your CIK value
* HINT: Obtain a CIK from https://renesas.exosite.com by clicking +Add Device
* NOTE: Your RDK should already have a CIK value associated, so this is just
        a disaster recovery setp and is not requried

4) Enable one of PMODAD4,PMODDA3, or PMODPOT at line 108~110 in the user-app.c

5) Compile and download -> check https://renesas.exosite.com to see your data
in the cloud!
* HINT: Your RDK must be connected to the Internet via the RJ-45 ethernet jack
* HINT: If your network does not support DHCP, you will need to edit the network
values in user_app.c (my_ip, my_netmask, my_default_router)

For more information on this project and other examples, reference the online 
documentation at http://tinyurl.com/28cphut

========================================
Release Info
========================================
----------------------------------------
Release 2012-03-15
----------------------------------------
--) initial version<br>

