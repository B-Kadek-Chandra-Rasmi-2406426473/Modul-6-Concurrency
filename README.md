## Commit 1 Reflection notes

## Commit 1 Reflection notes

Fungsi `handle_connection` bertugas secara spesifik untuk memproses aliran data dari koneksi TCP yang diterima server saat browser mengirimkan request. Di dalam fungsi ini, `TcpStream` dibungkus menggunakan `BufReader` untuk membaca data secara lebih efisien melalui mekanisme buffering. Selanjutnya, variabel `http_request` melakukan iterasi untuk membaca request HTTP baris demi baris dan mengumpulkannya ke dalam struktur data Vector. Proses pembacaan baris ini diinstruksikan untuk berhenti ketika menemukan baris kosong menggunakan `take_while`, karena baris kosong merupakan penanda standar berakhirnya bagian header pada HTTP request. Terakhir, request yang berhasil dibaca dicetak ke terminal menggunakan `println!`, memungkinkan verifikasi langsung terhadap detail informasi yang dikirimkan client seperti HTTP method (misalnya GET), Host, dan User-Agent.

