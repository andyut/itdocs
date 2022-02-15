# Membuat dokumentasi dalam Markdown

## Tujuan

* Memudahkan dokumentasi agar lebih terorganisasi.
* Bisa melakukan _full text search_
* Memenuhi standar dalam _techincal documentation_ ( Text based )
* Bisa diubah dalam format PDF HTML dll

## Aplikasi Yang digunakan

Untuk membuat  markdown bisa menggunakan editor 

* Stackedit : [https://stackedit.io/](https://stackedit.io/) 
* Typora : [https://typora.io/](https://typora.io/)
* VisualStudio Code : [https://code.visualstudio.com/](https://code.visualstudio.com/)
  * Plugin : _MarkdownAllInOne_
  * Plugin : _Markdown Preview Enhanced_


**Element	Markdown**

```markdown

# H1
## H2
### H3
Bold	**bold text**
Italic	*italicized text*
Blockquote	
> blockquote
Ordered List	
1. First item
2. Second item
3. Third item
Unordered List	- First item
- Second item
- Third item
Code	`code`
Horizontal Rule	---
Link	[title](https://www.example.com)
Image	![alt text](image.jpg)
```

## Menggunakan Mkdocs

**Keterangan**

Mkdocs merupakan site generator khusus untuk _Markdown_ File. Biasa digunakan untuk membangun dokumentasi proyek, dokumentasi source file, dan sebagainya.

Mkdocs menggabunggkan beberapa file markdown ( .md ), menjadi 1 site. dliengkapi dengan plugin Mermaid untuk flowchart, dan sebagainya.

**Instalasi**

Install menggunakan PIP

```bash
sudo pip install mkdocs

```
Kemudian Buat Folder untuk mkdocs

```ts
mkdocs new mydocumentation
```

Setelah selesai jalankan Mkdocs 

```bash
mkdocs serve 
```

Nanti akan keluar tampilan seperti ini

```bash
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 160402 15:50:43 server:271] Serving on http://127.0.0.1:8000
[I 160402 15:50:43 handlers:58] Start watching changes
[I 160402 15:50:43 handlers:60] Start detecting changes
```