Eksperimen 1: Stored XSS Attack
- alertnya tidak muncul
- komentar dari nama Hacker ada tetapi isi dari komentarnya tidak ada

Eksperimen 2: Image Tag XSS
karena tidak selalu harus ada tag script, selama ada atribut event maka javascript bisa dijalankan

Eksperimen 3: Cookie Stealing Simulation
- Cookie yang muncul: visitCount=20; sessionId=abc123xyz; username=JohnDoe
- ketika alert diganti menjadi fetch, tidak ada notifikasi saat komentarnya dikirim

Eksperimen 4: DOM Manipulation
halaman berubah menjadi merah

Eksperimen 5: Versi Secure
- yang berbeda adalah tidak ada notifikasi alert yang bisa membuat attacker masuk untuk mengambil data kita dan komentarnya muncul bersama kodenya
- berhasil

Eksperimen 6: Bandingkan Kode
Versi secure tidak vulnerable terhadap XSS karena aplikasi tidak memberi kesempatan input pengguna dijalankan sebagai kode. Karena di kode secure menggunakan beberapa teknik keamanan:
- textContent
- createElement
- Input Validation
- CSP Header

pertanyaan refleksi
1. karena onerror merupakan perintah otomatis yang dijalankan
2. 
- stored xss: itu adalah kode berbahaya yang disimpan attacker didalam server supaya setiap kali pengguna membuka  halaman web yang ada kode berbahaya tersebut maka akan otomatis menyerang pengguna yang mengaksesnya
- reflected xss: berbeda dengan stored xss, reflected xss tidak tersimpan didalam server melainkan saat pengguna mengakses request tertentu. seperti url atau form.
3. penting karena atribut httpOnly tidak bisa diakses oleh javascript
4. jangan menggunakan atribut seperti onerror agar tidak mudah di attack, lakukan penyaringan terhadap kode
5. CSP berfungsi sebagai lapisan keamanan tambahan yang membantu mengurangi dampak XSS dan serangan injeksi lainnya, meskipun masih ada celah di validasi input.

