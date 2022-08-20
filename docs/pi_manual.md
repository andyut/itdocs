# Pengajuan Ijin Import 

 ---

## Proses Pengajuan Ijin Import

**Master Data**

* Pihak Perijinan membuat daftar HS ( Master data HS )
* Pihak Perijinan membuat daftar persyaratan pengajuan ijin berdasarkan kategori komoditas
* Pihak Perijinan membuat daftar pelabuhan
* PIhak Perijinan membuat daftar negara yang akan diajukan 

**Proses Pengajuan Ijin**

**A. Dokumen Pengajuan**

* Purchasing membuat form pengajuan ijin import berdasarkan kategori komoditas yang dibuat oleh perijinan
* Purchasing menentukan negara-negara tujuan untuk ijin import
* Purchasing menentukan  _Rekom_ apa saja untuk mendapatkan ijin.
* Purchasing menentukan item barang yang diajukan untuk mendapatkan ijin import berdasarkan nomor HS
* Purchasing mengenerate syarat syarat pengajuan berdasarkan kategori komoditas dari perijinan
* Status form menjadi ```Draft```
* Purchasing mengupload semua dokumen yang diperlukan, berdasarkan list `` syarat pengajuan ijin ``
* Setelah semua dokumen berhasil di upload status berubah menjadi ``Waiting for validation``
* Purchasing menyimpan form tersebut dan print sebagai ``Dokument Pengajuan Ijin`` yang kemudian di ttd oleh --direksi terkait--
* Status Form Menjadi ```Waiting for validation-Printed```
* Akan keluar notifikasi email ke **perijinan@indoguna.co.id**

**B. Verifikasi dokumen**

* Pihak perijinan memverifikasi semua dokumen yang diupload oleh pihak purchasing
* Setelah semua dokumen terverifikasi, pihak perijinan menekan tombol ``[Start]`` untuk memulai proses pengajuan ijin
* Status dokumen berubah menjadi ``Start Progress`` dan akan ada notifikasi ke **perijinan@indoguna.co.id**


---
## Proses Penerbitan Ijin Import


* Pihak perijinan membuat form penerbitan PI dari menu pengajuan Ijin ( yang status nya _on Progress_  atau _Start Progress_ )
* Pilihan _rekom_ di menu pengajuan ijin akan berubah menjadi list task di form penerbitan PI. Jumlah task ini akan digunakan untuk menghitung _persentasi proses penerbitan Ijin_
* Pihak perijinan menyesuaikan HS Item , dan negara yang akan diajukan. 
* Setelah tersimpan dokumen pengajuan akan berubah dari ``Start Progress`` menjadi ``on Progress`` dan dokumen penerbitan ijin statusnya menjadi ```Process```, dan persentase proses mulai dihitung dari 


$\left(\frac{ 1} {([Jumlah Task] + 1 )}  \times 100 \right)$


* Pihak Perijinan akan mengupload setiap dokumen _rekom_ yang sudah jadi, jika semua sudah komplit, status akan berubah menjadi ``Complete``
* Setelah dokumen berubah menjadi ``Complete`` akan muncul tombol ``[DONE]`` Untuk closed dokumen tersebut, sehingga dokumen tersebut tidak bisa diubah.

