# WMS SAP INDOGUNA
    


## SETUP SAP

**Format Warehouse**

Skema Warehouse Indoguna 

6 level  structure :
 
* Location
* Warehouse
* Gate
* Rack
* Row
* Bin

**[Location]**

| Location | Location Code |
|---|---|
| Gudang IGU  | A |
| Gudang IGU Cikupa | B |
| Gudang Makasar | C |
| Gudang Bandung | D |
| Gudang Jogja | E |
| Gudang Semarang | F |
| Gudang Surabaya | G |
| Gudang Bali | H |
| Gudang Balikpapan | I |
| Gudang Palembang | J |

<br/>

**[warehouse]**

| Warehouse | Warehouse Code |
|---|---|
| Pondok Bambu Gdg Baru | A1 |
| Pondok Bambu Gdg Lama | A2 |
| Pondok Bambu Gdg Pork | A3 |
| Cikupa IGU | B1 |
| Cikupa IMS | B2 |
| Cikupa BWN | B3 |
| Cikupa SARKUL | B4 |
| Gudang Makasar | C1 |
| Gudang Bandung | D1 |
| Gudang Jogja | E1 |
| Gudang Semarang | F1 |
| Gudang Surabaya | G1 |
| Gudang Bali | H1 |
| Gudang Balikpapan | I1 |
| Gudang Palembang | J1 |

**[Gate]**

format code 
* G01 s/d G12
* F01 s/d F20
* ARB - ARD (anteroom )

**[Rack]**

format Code : R01 - R24

**[Row]**

format Code : 01 - 33


**[Bin]**

format Code : A1 - G2

**[Format Code Bin Location]**

example : Pondok Bambu Gdg Baru gate 01 Rack 01 

    A1G01-R01-01-A1
    A1G01-R01-01-A2
    A1G01-R01-01-B1
    A1G01-R01-02-A1
    A1ARB-R01-00-00


example : Palembang gate F02 Rack 02

    J1F02-R02-01-A1
    J1F02-R02-01-A2
    J1F02-R02-01-B1
    J1F02-R02-02-A1
    J1ARC-R00-00-00


