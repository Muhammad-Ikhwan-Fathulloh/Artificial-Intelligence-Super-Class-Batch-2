# **📖 Panduan Lengkap: Otomatisasi Analisis PDF dengan Make.com**  
**🔹 Tujuan:**  
✅ Ekstrak teks dari file PDF  
✅ Analisis teks dengan AI (Gemini/OpenAI)  
✅ Simpan hasil ke Google Sheets / Notion  
✅ Kirim notifikasi melalui Email atau Slack  

---

## **🛠 1. Persiapan: Akun & Tools yang Dibutuhkan**  
Sebelum memulai, pastikan kamu sudah memiliki:  
✅ **Akun Make.com** ([Daftar di sini](https://www.make.com/))  
✅ **Akun Google Drive** (untuk menyimpan PDF)  
✅ **Akun OpenAI atau Gemini** (untuk analisis AI)  
✅ **Google Sheets / Notion** (untuk menyimpan hasil)  

---

## **🚀 2. Membuat Workflow di Make.com**  

### **🔹 Langkah 1: Trigger - Upload PDF ke Google Drive**  
1️⃣ Buka **Make.com** → Klik **Create a new scenario**  
2️⃣ Tambahkan **Google Drive → Watch Files**  
   - Pilih folder tempat file PDF diunggah  
   - Set trigger untuk berjalan otomatis saat ada file baru  

📌 *Alternatif:* Jika PDF dikirim via email, gunakan **Gmail → Watch Emails** untuk mendeteksi attachment PDF.  

---

### **🔹 Langkah 2: Ekstrak Teks dari PDF**  
1️⃣ Tambahkan modul **PDF.co → Extract Text**  
2️⃣ Pilih **File dari Google Drive** sebagai input  
3️⃣ Atur output ke format **Plain Text**  

✅ *Hasil:* Teks dari PDF berhasil diekstrak.  

---

### **🔹 Langkah 3: Analisis AI (Ringkasan & Klasifikasi)**  
1️⃣ Tambahkan modul **OpenAI → ChatGPT (Text Completion)**  
2️⃣ Masukkan teks dari PDF sebagai input  
3️⃣ Gunakan prompt berikut:  
   ```
   Tolong buat ringkasan dari dokumen ini, tentukan kategori dokumen, dan ekstrak entitas utama (nama, tempat, topik, dll.).
   ```
4️⃣ **Hasil Output:**  
   - **Ringkasan Dokumen**  
   - **Kategori Dokumen**  
   - **Entitas Utama**  

📌 *Alternatif:* Jika menggunakan **Google Gemini**, gunakan **Google AI → Text Generation**.  

---

### **🔹 Langkah 4: Simpan Hasil ke Google Sheets / Notion**  
✅ **Pilih tempat penyimpanan hasil analisis:**  
1️⃣ **Google Sheets → Add Row**  
   - **Kolom:** Nama File, Ringkasan, Kategori, Entitas  
2️⃣ **Notion → Add Database Item**  
   - Tambahkan data ke Notion Database untuk dokumentasi lebih rapi  

✅ *Hasil:* Semua data otomatis tersimpan tanpa perlu input manual.  

---

### **🔹 Langkah 5: Kirim Notifikasi via Email / Slack**  
1️⃣ **Gmail / Outlook → Send Email**  
   - **Subject:** 📄 **Analisis PDF Selesai!**  
   - **Body:** Menampilkan ringkasan dokumen dan insight utama  
2️⃣ **Slack → Send Message**  
   - Kirim laporan analisis ke channel tertentu  

✅ *Hasil:* Notifikasi otomatis terkirim ke tim atau pengguna.  

---

## **✅ 3. Hasil Akhir: Workflow Otomatis Berjalan!**  
📂 **Upload PDF** → 📝 **Ekstrak teks** → 🤖 **Analisis AI** → 📊 **Simpan ke Google Sheets / Notion** → 📩 **Kirim laporan ke Email / Slack**  