ID	Rule
BR-001	Order harus memiliki minimal satu item
BR-002	Quantity setiap item harus lebih besar dari nol
BR-003	Order hanya dapat diproses jika produk valid
BR-004	Stok harus tersedia untuk reservasi
BR-005	Payment hanya diproses setelah stok berhasil direservasi
BR-006	Order hanya dikonfirmasi setelah payment berhasil
BR-007	Payment gagal menyebabkan order dibatalkan sesuai kebijakan bisnis
BR-008	Stok yang sudah direservasi harus dilepaskan ketika order dibatalkan
BR-009	Order yang sudah confirmed tidak boleh dibatalkan menggunakan proses pembatalan biasa
BR-010	Setiap order memiliki identifier unik