# Perbaikan AR - Invoice

---

## Sebelum
---

### ALUR 

**Admin DO**

* Menerima dokumen DO dari bagian admin gudang
* cek semua kelengkapan dokumen untuk syarat tagih
* Check list di sistem kelengkapan tersebut (```cnw-dolist```)

**Invoice**

* Membuat invoice berdasarkan dokumen yang diberikan dari bagian admin
* setelah selesai, bagian invoice akan print dokumen tersebut untuk digabungkan dengan dokumen lain
    * _jika status print invoice aktif_

**Admin Invoice**
* Menggabungkan semua dokumen terkait ( ```invoice checklist```)
* memberikan ke bagian kwitansi

**Admin Kwitansi**

* membuat dan print kwitansi
* print list kwitansi
* Serahkan kembali dokumen plus kwitansi

**Admin Invoice**

* Stampel dan cek ulang kelengkapan dokumen
* Menyiapkan dokumen untuk diturunkan ke bagian AR
* Menurutkan dokumen ke bagian AR



---

## Perbaikannya
---

### ALUR  


**Admin DO**

* Menerima dokumen DO dari bagian admin gudang
* cek semua kelengkapan dokumen untuk syarat tagih ( berdasarkan ```jadwal tukarfaktur```)
* Check list di sistem kelengkapan tersebut (```cnw-dolist```)
* Scan dan ___Upload GR dan dokumen dari customer (DO asli)___ ke system (```cnw-dolist```)

**Invoice**


* Membuat invoice berdasarkan dokumen yang diberikan dari bagian admin
* setelah selesai, bagian invoice akan print dokumen tersebut untuk digabungkan dengan dokumen lain
    * _jika status print invoice di business partner aktif_
* Cek DO yang belum dibuatkan invoice/faktur berdasarkan ```jadwal tukar faktur```,jika dokumen penunjang (DO, GR, PO) tidak ada, maka segera minta bagian admin do untuk urus (```check status = request dok DO```)



**Admin Invoice**


* Menggabungkan semua dokumen terkait ( ```invoice checklist```), berdasarkan prioritas dari _jadwal tukar faktur_
* kemudian dikelompokkan berdasarkan jadwal dan ar (grouping jadwal dan ar)
* memberikan ke bagian kwitansi untuk dibuatkan kwitansi


**Admin Kwitansi**

* membuat dan print kwitansi berdasarkan dok yang diberikan
* print list kwitansi ___berdasarkan AR___ dan tanggal kwitansi
* Serahkan kembali dokumen dengan kwitansi, dokumen lengkap, ___dikelompokkan berdasarkan AR___ dengan diatasnya cetakan ___"list kwitansi per AR"___

**Admin Invoice**

* Stampel dan cek ulang kelengkapan dokumen
* Menurutkan dokumen ke bagian AR, per kotak / bagian yang sesuai dengan nama AR nya 



