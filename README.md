# Real-Time Video Analytics — Speed Estimation & Historical Insight

Link Collab : [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/drive/11ZP_fdsYADDBYcXbw2Hq3moOdP9jUEWp?usp=sharing
)

Notebook ini mendemonstrasikan penerapan **real-time video analytics** menggunakan computer vision untuk:
- object detection & tracking
- speed estimation berbasis world coordinate
- geofencing (IN / OUT)
- historical vehicle presence counting
- visual insight overlay pada video

Pipeline dirancang dengan pendekatan **historical insight**, bukan event-based transactional counting.

---

## 🎯 Objective

Tujuan utama notebook ini adalah:
- mengekstrak **informasi pergerakan kendaraan** dari video
- mengestimasi **kecepatan kendaraan** secara real-time
- mengumpulkan **insight historikal** kendaraan yang pernah muncul di zona tertentu
- menyajikan hasil dalam bentuk **visual dashboard overlay**

Notebook ini ditujukan sebagai:
- proof of concept (PoC)
- bahan riset
- referensi implementasi industri (CCTV / traffic analytics)

---

## 🧠 Key Concepts

- **Object Detection**  
  Menggunakan model YOLO untuk mendeteksi kendaraan (car, bus, truck).

- **Multi-Object Tracking**  
  Menggunakan ByteTrack untuk menjaga konsistensi ID antar frame.

- **Speed Estimation**  
  Kecepatan dihitung dari perpindahan posisi objek di dunia nyata dengan transformasi pixel → meter menggunakan homography.

- **Geofencing**  
  Zona IN dan OUT digunakan untuk:
  - validasi lintasan
  - segmentasi analisis
  - agregasi insight historikal

- **Historical Presence Counting**  
  Sistem menghitung **ID unik kendaraan yang pernah muncul di zona**, bukan jumlah event crossing.
