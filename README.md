# **Text Sentiment Analysis using Caikit and Hugging Face**

## Overview
Proyek ini menganalisis text dengan menggunakan Caikit dan Hugging Face

## Requirements

To run this project, you will need:
- Linux/MacOS x86_64 
- Caikit (v0.9.2)
- Python (v3.8+)
- pip (v23.0+)
  
# Project Structure
text-sentiment/                      => package directory <br>
│<br>
├── start_runtime.py                 => wrapper yang memulai runtime Caikit sebagai server gRPC, ini akan memuat model saat startup.<br>
├── client.py                        => klien akan memanggil runtime Caikit untuk untuk melakukan analisis sentimen.<br>
├── requirements.txt                 => library yang dibutuhkan.<br>
├── models/                          => subdirectory berisi metadata caikit dan artifacts yang diperlukan.<br>
│   └── text_sentiment/config.yml#   => Caikit model sentiment data.<br>
├── text_sentiment/                  => berisi modul caikit, implementasi algoritma train/run AI model.<br>
│   ├── config.yml                   => konfigurasi model.<br>
│   ├── __init__.py                  => <br>
│   ├── data_model/                  => format data Caikit.<br>
|       ├── classification.py        => Kelas data yang menjadi atribut model AI.<br>
│       └── __init__.py              => <br>
│   └── runtime_model/               => Caikit modul.<br>
|       ├── hf_module.py             => Bootstrap model AI.<br>
│       └── __init__.py               

## Procedur
1. Instal runtime Caikit
   
   ```bash
   pip install --user virtualenv
   
2. Buat proyek
3. Buat spesifikasi model data
4. Buat pembungkus model
5. Sertakan modul dan ketergantungan paket
6. Mulai runtime Caikit
7. Uji analisis sentimen <br>

   Run project:
    ```bash
    cd /home/project/text-sentiment/
    source env/bin/activate
    python client.py
    
Result :
![Screenshot 2024-11-05 181406](https://github.com/user-attachments/assets/1b1ba957-97a2-41fe-97e5-f288f164f40d)

Conclusion:
Model AI ini masih harus di training atau diperbaiki datanya karena beberapa kalimat yang seharusnya positive, malah menjadi negative. Seperti kalimat "saya sangat suka hujan", padahal sudah ada kata "suka", tetapi 
outputnya tetap negative.
