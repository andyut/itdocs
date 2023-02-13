#  Sistem Tokopedia

## Prosedur


* User invoice menarik delivery Order yang masih terbuka, berdasarkan nomor invoice ```TOKOPEDIA```
  * beberapa delivery dibuatkan **1 Invoice** berdasarkan 1 nomor invoice tokopedia

* User Invoice memerika total nilai dokumen sama dengan invoice tokopedia. jika tidak sama, user invoice **menyamakan** nilai invoice tokopedia sama dengan total invoice SAP.
  * Total promo = discSum ( total discount )
  * Total invoice = DocSum - DiscSum + PPn
* User Invoice melakukan ```[Calculate 1]``` untuk membagi nilai promo (discsum) prorate ke masing masing item barang
  * Nilai discsum diset = 0, nilai discsum di bagi ke perbarang.
  * Setelah dibagi ke barang secara prorate ( by LineTotal ), nilai LineTotal = LineTotal - TotalLinePromo
* User Invoice melakukan ```[Calculate 2]``` untuk menghitung nilai service fee berdasarkan jenis barang.
* User cek ulang secara total setelah service fee = total sebelum promo 
* Jika semua sudah sesuai user tekan tombol ```POST TO SAP```



