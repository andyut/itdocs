# Integrasi Efaktur vs SAP

    Link file PDf Efaktur ke dalam OINV (invoice) di cbw


## Tahapan


**Komputer Efaktur**


1. export PDF ke folder yang ditentukan tiap hari 
2. Update / sync folder tersebut ke server 
   Program Rsync, DeltaCopy, filezilla, atau yang lain.

**Server**


1. Jalankan update file list ke CNW, untuk data list file terupdate
2. Sync dengan cnw-invoice-list, berdsasarkan no faktur pajak vs nama file faktur pajak


**Cara User akses Efaktur**

1. download individual efaktur dari ```invoice List```
2. Checklist Invoice dari ```invoice List``` , kemudian download dalam 2 opsi format 
   * ZIP file ( multi file pdf) : Menggunakan ```from zipfile import ZipFile```
   * PDF ( merge multi file pdf jadi 1 file) : ```from PyPDF2 import PdfFileMerger```
