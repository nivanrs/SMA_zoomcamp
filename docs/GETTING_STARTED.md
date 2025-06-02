# Panduan Memulai Zoomcamp Analisis Pasar Saham

Dokumen ini memberikan informasi penting untuk membantu Anda memulai perjalanan belajar di "Stock Market Analytics Zoomcamp". Meliputi persyaratan dasar, cara mengatur lingkungan, dan akses ke materi kursus.

## Persyaratan Dasar

Untuk mendapatkan manfaat maksimal dari kursus ini, disarankan Anda memiliki:

- Pemahaman dasar tentang bahasa pemrograman Python.
- Kenal dengan konsep dasar data.
- Akun Google untuk mengakses notebook Google Colab.

## Mengatur Lingkungan

Kursus utamanya menggunakan Google Colab untuk latihan praktis. Untuk modul terakhir (Module 5), Anda perlu mengatur lingkungan lokal jika ingin menjalankan automasi.

### Google Colab

Sebagian besar contoh kode di kursus disajikan sebagai notebook Google Colab. Anda bisa mengaksesnya langsung melalui link di dokumen modul masing-masing. Colab menyediakan lingkungan Jupyter di cloud, sehingga tidak perlu pengaturan tambahan untuk notebook.

### Pengaturan Lingkungan Lokal (untuk Module 5)

Untuk Module 5, Anda akan beralih ke file Python lokal dan mungkin perlu mengatur lingkungan pengembangan lokal.

1.  **Ubah Direktori Kerja:**

    ```bash
    cd source/stock-markets-analytics-zoomcamp/05-deployment-and-automation/
    ```

2.  **Instal Virtual Environment:**

    ```bash
    pip3 install virtualenv
    ```

3.  **Buat Virtual Environment Baru (venv):**

    ```bash
    virtualenv venv
    # ATAU
    python3 -m venv venv
    ```

4.  **Aktifkan Virtual Environment:**

    - **Linux/macOS:**
      ```bash
      source venv/bin/activate
      ```
    - **Windows (Command Prompt):**
      ```bash
      venv\Scripts\activate
      ```
    - **Windows (PowerShell):**
      ```powershell
      .\venv\Scripts\Activate.ps1
      ```

5.  **Instal Ta-lib (Library Analisis Teknik):**

    - **Untuk macOS:**
      - **Langkah 1: Instal Homebrew** (jika belum terinstal):
        ```bash
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        ```
      - **Langkah 2: Instal TA-Lib menggunakan Homebrew:**
        ```bash
        brew install ta-lib
        ```
      - **Langkah 3: Instal package ta-lib Python** (pastikan virtual environment aktif):
        ```bash
        pip3 install ta-lib
        ```
      - **Langkah 4: Pastikan kompatibilitas versi Numpy:** Pastikan Anda menggunakan versi Numpy sebelum versi 2 (misalnya "numpy==1.26.4" di `requirements.txt`) agar `ta-lib` dapat di-import dengan lancar. Lihat [link ini](https://stackoverflow.com/questions/78634235/numpy-dtype-size-changed-may-indicate-binary-incompatibility-expected-96-from) untuk detail lebih lanjut.
    - **Untuk sistem operasi lainnya**, silakan lihat petunjuk instalasi resmi TA-Lib.

6.  **Instal semua requirements ke environment baru (venv):**
    ```bash
    pip3 install -r requirements.txt
    ```

### Menjalankan Proyek (Lokal)

Setelah mengatur lingkungan lokal dan mengaktifkan virtual environment:

- **Mulai Server Jupyter Lokal:**
  ```bash
  jupyter notebook
  ```
  (Anda bisa cek semua server yang berjalan dengan `jupyter notebook list`)
- **Buka `test.ipynb` untuk memeriksa sistem:**
  - Dari browser web (buka `http://localhost:8888/tree` atau sejenisnya).
  - Atau melalui antarmuka VS Code (tentukan kernel server address).
- **Jalankan `main.py` dari Terminal (atau Cron) untuk mensimulasikan satu hari data baru:**
  ```bash
  python main.py
  ```

## Akses Materi Kursus

Semua materi kursus tersedia secara gratis:

- **Rekaman YouTube:** Setiap modul memiliki rekaman siaran langsung yang sesuai. Link disediakan di dokumen modul masing-masing.
- **Slide:** Slide presentasi untuk setiap modul tersedia melalui link Google Slides.
- **Kode di Colab:** Notebook Jupyter interaktif yang dihosting di Google Colab disediakan untuk latihan coding.
- **Tugas Rumah:** Ditemukan di folder `cohorts/` untuk tahun yang sesuai. Link pengiriman dan deadline disediakan di sana.
