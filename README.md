# Pixel Fighter - cara membuat APK lewat GitHub

## Isi folder
- `www/index.html`  -> game-nya (satu file)
- `capacitor.config.json`, `package.json` -> pembungkus aplikasi
- `.github/workflows/build-apk.yml` -> robot GitHub yang membuat APK otomatis

## Langkah
1. Buat repository baru di GitHub (boleh private).
2. Upload SEMUA isi folder ini ke repository, termasuk folder `.github` (folder berawalan titik).
   Paling mudah lewat komputer: GitHub Desktop, atau `git push`.
3. Buka tab **Actions** -> workflow **Build APK** -> tunggu sampai hijau (sekitar 5-10 menit).
   Kalau tidak jalan sendiri: **Run workflow**.
4. Buka run yang berhasil -> bagian **Artifacts** -> unduh `pixel-fighter-apk` (isinya `app-debug.apk`).
5. Pindahkan ke HP Android, buka, izinkan "install dari sumber tidak dikenal", lalu install.

## Memperbarui game
Ganti `www/index.html` dengan versi baru, commit, push. APK baru dibuat otomatis.

## Catatan
- APK ini versi debug (untuk dipakai sendiri / dibagikan ke teman). Untuk Google Play perlu tanda tangan rilis (signing) - bisa ditambahkan nanti.
- Font Google memerlukan internet. Offline, game memakai font cadangan (Impact / Arial Black).
- Kalau build gagal (merah), buka log langkah yang gagal dan kirim teksnya ke Claude.
