# Projek-PSBI

Proyek Django sederhana untuk LMS (Learning Management System).

## Ringkasan
Aplikasi ini adalah proyek Django (lihat `manage.py` dan `lms_project/`). Database default: SQLite (`db.sqlite3`).

## Persiapan dan menjalankan lokal

1. Buat virtual environment dan aktifkan:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

2. Pasang dependensi:

```bash
pip install -r requirements.txt
```

3. Migrasi database dan jalankan server:

```bash
python manage.py migrate
python manage.py runserver
```

4. Jalankan test:

```bash
pytest
```

## Catatan deploy
- Aplikasi ini dibuat sebagai aplikasi Django. Untuk deploy rekomendasi: Render, Heroku, atau VPS (Gunicorn + nginx).
- Jika tujuan Anda adalah menjadikan antarmuka sebagai aplikasi Streamlit, aplikasi perlu ditulis ulang ke `streamlit_app.py`. Beritahu saya jika Anda ingin saya buatkan versi Streamlit.

## Streamlit preview
Saya menambahkan `streamlit_app.py` — sebuah helper kecil untuk melihat template dan file statis tanpa menjalankan Django. Untuk menjalankan:

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
```

## File penting
- `manage.py` — entrypoint Django.
- `lms_project/` — konfigurasi project.
- `dashboard/` — aplikasi utama dengan templates dan static files.

## Lisensi
Lisensi MIT (file `LICENSE`).
