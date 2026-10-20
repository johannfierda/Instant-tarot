# Tarot Instan - proyek APK (Capacitor)

## Cara 1: tanpa komputer khusus (GitHub Actions)
1. Buat repositori GitHub baru, unggah semua isi folder ini (termasuk folder .github).
2. Tab Actions > "Build APK" > Run workflow.
3. Setelah selesai (sekitar 5-8 menit), unduh artifact "tarot-instan-apk" (berisi app-debug.apk).
4. Salin ke ponsel, izinkan "Instal dari sumber tidak dikenal", lalu instal.

## Cara 2: Android Studio
1. Pasang Node.js 20, JDK 17, Android Studio.
2. npm install
3. npx cap add android
4. Tambahkan <uses-permission android:name="android.permission.CAMERA" /> di android/app/src/main/AndroidManifest.xml
5. npx cap sync android
6. npx cap open android > Build > Build APK(s)

## Memakai aplikasi
Buka aplikasi, isi Kunci API Anthropic (console.anthropic.com) di layar awal. Kunci disimpan di perangkat.
Model dapat diganti lewat konstanta MODEL di www/index.html.

## Catatan keamanan
Kunci API di dalam aplikasi hanya cocok untuk pemakaian pribadi. Untuk dibagikan ke publik, buat server proxy
yang menyimpan kunci, lalu ubah URL di fungsi AI().
