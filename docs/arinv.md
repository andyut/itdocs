# Perbaikan Sistem AR - Invoice

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

**AR**

* Membuat jadwal tukar faktur per customer disertai keterangan syarat tukar faktur (```CNW-BP```)
* Memasukkan nama kolektor per customer
* _Men-setting aturan cetak kwitansi, invoice , dan faktur pajak_ per customer
  * Status print invoice ( Y / N )
  * Status print Faktur pajak ( Y / N )
  * Status print kwitansi ( Y / N)
  * _```Status Cetakan Kwitansi ( per Code Customer / Per Outlet )```_



**Admin DO**

* Menerima dokumen DO dari bagian admin gudang
* cek semua kelengkapan dokumen untuk syarat tagih ( berdasarkan ```jadwal tukarfaktur```)
* Check list di sistem kelengkapan tersebut (```cnw-dolist```)
* Scan dan ___Upload GR dan dokumen dari customer (DO asli)___ ke system (```cnw-dolist```)

**Invoice**


* Membuat invoice berdasarkan dokumen yang diberikan dari bagian admin
* setelah selesai, bagian invoice akan print dokumen tersebut untuk digabungkan dengan dokumen  (DO )
    * _jika status print invoice di business partner aktif_
* Cek DO yang belum dibuatkan invoice/faktur berdasarkan ```jadwal tukar faktur```,jika dokumen penunjang (DO, GR, PO) tidak ada, maka segera minta bagian admin do untuk urus (```check status = request dok DO```)
* Setelah menggabungkan dokumen DO dan invoice, dokumen tersebut di serahkan ke bagian kwitansi


**Admin Kwitansi**

* Invoice yang diterima discan sebagai tanda terima invoice
* Setelah discan, invoice dikelompok kan berdasarkan kategori
  * Tukar Faktur
  * Tidak Tukar Faktur
  * Harian
  * PIA
  

* jika ada jadwal tf dikelompokkan terlebih dahulu untuk jadwal besok hari ( dilihat di sistem list kwitansi-> jadwal tukar faktur) --> masuk ke kategori harian
* jika tidak ada tukar faktur maka dipisahkan ke dalam box tidak tukar faktur
* User kwitansi mengenerate otomatis kwitansi tidak berdasarkan customer, tetapi berdasarkan jadwal harian TF

> Contoh : untuk hari jumat, user kwitansi akan tekan tombol generate untuk jadwal jumat, dan memasukan _tanggal_. Maka sistem akan otomatis generate nomor kwitansi berdasarkan __invoice yang sudah di ceklist__ dikelompokkan berdasarkan _kode customer, Tipe cetakan( perkode customer atau per outlet)_.

* User Kwitansi print kwitansi
  * berdasarkan status print [Y/N] , jika tidak maka tetap tidak akan tercetak walau dimasukkan nomor kwitansinya
* User kwitansi akan menggabungkan kwitansi dengan DO fakturnya.
* User kwitansi akan print list kwitansi berdasarkan AR atau group yang di tentukan
* User kwitansi akan ```mengurutkan dan mengelompokkan```  nomor kwitansi berdasarkan list kwitansi 
* List kwitansi tersebut ditempel diatas gabungan kwitansi dan invoice
* Semua dokumen setelah di tempel **list kwitansi** diserahkan ke bagian Admin invoice

**Admin Invoice**

* Setelah menerima dokumen dari bagian kwitansi, dokumen tersebut di Stampel dan cek ulang kelengkapan dokumen berdasarkan list kwitansi
* Menurutkan dokumen ke bagian AR ( sudah dikelompokkan per list kwitansi per AR)



