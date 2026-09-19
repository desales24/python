# Setup Python — Diagram Flowchart

Panduan singkat untuk menjalankan script pembuat diagram alur menggunakan Python di WSL Ubuntu.

## Requirement

- WSL2 dengan Ubuntu
- Python 3 (biasanya sudah terpasang default di Ubuntu)

## 1. Update daftar paket

```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Install Python & tools pendukung

```bash
sudo apt install python3 python3-pip python3-venv -y
```

Cek versi untuk memastikan sudah terpasang:

```bash
python3 --version
pip3 --version
```

## 3. Buat virtual environment

Masuk ke folder project, lalu jalankan:

```bash
python3 -m venv venv
```

## 4. Aktifkan virtual environment

```bash
source venv/bin/activate
```

Prompt terminal akan berubah, biasanya muncul `(venv)` di depan — tandanya environment sudah aktif.

## 5. Install dependency

```bash
pip install matplotlib
```

Atau, jika sudah punya file `requirements.txt`:

```bash
pip install -r requirements.txt
```

## 6. Jalankan script

```bash
python3 nama_file.py
```

Atau buka file `.ipynb` di Jupyter Notebook / VS Code kalau kodenya dalam bentuk notebook.

## 7. Nonaktifkan environment (opsional)

Setelah selesai:

```bash
deactivate
```

## Catatan

- Kalau muncul error `externally-managed-environment` saat `pip install` di luar venv, itu normal di Ubuntu versi baru — solusinya selalu install package di dalam virtual environment.
- Untuk menyimpan daftar dependency agar mudah di-setup ulang, gunakan:

  ```bash
  pip freeze > requirements.txt
  ```
