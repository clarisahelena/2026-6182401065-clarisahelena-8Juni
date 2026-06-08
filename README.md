## Mekanik Permainan & Fitur Spesifik

### Toleransi Deteksi Game Over (Grace Period 1 Detik)
Untuk mencegah *Game Over* instan saat pemain baru saja menjatuhkan objek dari atas layar, game ini menerapkan waktu toleransi (Grace Period) selama 1 detik.

* **Cara Kerja:** Setiap kali burung dijatuhkan, sistem akan mencatat waktu mulainya (*timer* dimulai dari 0 saat *touch end*). 
* **Aturan Batas Atas:** Jika posisi burung berada di atas garis batas akhir (`gameOverYThreshold`), permainan tidak akan langsung berhenti. Sistem memberikan jeda aman selama **1.0 detik**. Jika setelah 1 detik objek masih menyangkut atau melewati batas atas tersebut, barulah status *Game Over* terpicu.
