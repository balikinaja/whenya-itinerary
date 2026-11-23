VOYAGE V2 — PATCH UAT (belum deploy)

Perubahan dalam paket ini:
- Menu Edit / Duplicate / Soft Delete / Restore trip untuk pemilik.
- Filter Recently Deleted.
- Favicon SVG dan manifest.
- Hapus label Firebase di layar normal (pesan error tetap tampil).
- Deteksi jadwal bentrok bila kedua aktivitas memiliki jam selesai.
- Export PDF via jendela print browser (pilih Save as PDF).

Fitur yang SUDAH ada di source awal: jam mulai/selesai dan durasi aktivitas, dashboard countdown, budget, split bill, packing checklist, share undangan dengan approval.

BELUM DILAKUKAN:
- Uji end-to-end terhadap Firebase nyata.
- Audit dan update Firestore Security Rules (tidak ada dalam ZIP).
- Packing template otomatis, estimasi vs aktual per kategori, dan share read-only.
- Ikon PNG 192/512 untuk kompatibilitas PWA penuh.

PENTING: Jangan deploy langsung ke situs utama. Test di branch terpisah dan preview terlebih dahulu. Soft delete hanya mengubah deletedAt, tidak menghapus dokumen atau subkoleksi. Firestore Rules harus menegakkan akses pemilik untuk perubahan delete/restore.
