# Pembelian expense

## ALUR 

### GA

**Rule:**

pembelian barang rumah tangga
    * kebutuhan pantri
    * tissue 


ATK

kertas 
      * printer

 ---

* bu_klara request  ke pak sima
* pak sima order ke vendor 
* nabila receive bandingkan dengan order


**request - order - invocing - bayar**

```mermaid
flowchart TD

A[Clara] -.request.-> B[sima]
B -.order.-> C[[vendor]]
C --receiving--> D(Nabila)
D -.invocing.-> A

```

**order - payment - invocing - reimburs**

```mermaid
flowchart TD

A[Clara] -.direct buying.-> B[market]
B -.request & PO.-> C[sima]
B --receiving--> D(Nabila)
C -.invocing.-> E[accounting]
E -.Reimburs.-> A

```

test
