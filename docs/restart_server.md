#  Restart Server pendukung SAP


---

### Server Order List

**IP :** 192.168.250.34
**User :**  Administrator
**Password :** a
**Connection :** RDP

**RESTART IIS SERVER**

**Opsi 1** 


![Sales Order List iis Reset](img/09_iisreset.png)


* Masuk ke command prompt
    * Ketik " _iisreset_  "


**Opsi 2**

![Sales Order List iis Menu](img/09_iis_menu.png)
* Masuk ke IIS
    * Click kanan di website
    * Pilih Restart / Stop & Start

**STOP IIS SERVER**
* Masuk ke IIS
    * Click kanan di website
    * Pilih Stop 





---

### Server Web SAP

**IP :** 192.168.250.13
**User :**  Administrator
**Password :** password#01
**Connection :** RDP

**RESTART IIS SERVER**

Internet Information Server -> web site

![ iis Menu](img/32IISMENU.png)


![ iis Menu](img/32IISMENU2.png)


* Restart Services

![ iis Menu](img/32IISMENU3.png)




---

### Server CNW

**IP :** 192.168.250.14
**User :**  admin
**Password :** admin
**Connection :** SSH
(user Windows untuk login menggunakan Putty)

**RESTART Services**
 

* masuk terminal
    * ketik `sudo systemctl restart odoo-invoice.service`


![ CNW Menu](img/CNWRESTART.png)


---

### Server Tally

**IP :** 192.168.250.15
**User :**  admin
**Password :** 19u7@m4it
**Connection :** SSH
(user Windows untuk login menggunakan Putty)

**RESTART Services**
 

* masuk terminal
    * ketik `sudo systemctl restart odoo-cnw.service`



![ CNW Menu](img/TALLYRESTART.png)
