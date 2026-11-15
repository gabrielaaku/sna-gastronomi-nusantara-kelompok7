# Jaringan Ko-kemunculan Bahan Masakan Nusantara - Kelompok 7

## Bahasa Indonesia

### Ringkasan dataset
Jaringan tidak berarah dan berbobot. Simpulnya adalah bahan masakan, dan sisinya menghubungkan dua bahan yang muncul dalam resep yang sama. Bobot sisi menyatakan jumlah resep yang memuat pasangan bahan tersebut.

| Ukuran | Pilot (13–14 Nov 2026) |
|---|---|
| Sumber | Cookpad Indonesia, pencarian "rendang" - https://cookpad.com/id/cari/rendang |
| Jumlah resep | 60 |
| Simpul (bahan unik, label mentah) | 233 |
| Sisi | 2.343 |
| Berarah / berbobot | Tidak / Ya |
| Uji 5 masakan daerah lain | gudeg, rawon, woku, ayam betutu, soto betawi (10 resep per masakan) |
| Setelah normalisasi (rendang + 5 daerah) | 109 resep, 97 bahan, 1.751 sisi |

### Berkas
| Berkas | Isi |
|---|---|
| `recipes_raw.json` | Data mentah rendang: url, judul, dan daftar bahan per resep |
| `nodes.csv` | `id, label` |
| `edges.csv` | `source, target, weight` |
| `notebook.ipynb` | Kode scraping, normalisasi, pembentukan jaringan, statistik pilot, dan metadata |
| `recipes_multidaerah.json` | Uji 5 masakan daerah lain, 10 resep per masakan |
| `output_clean/` | Jaringan setelah normalisasi nama bahan: `nodes_clean.csv`, `edges_clean.csv`, `mapping_bahan.csv`, `ringkasan_normalisasi.csv`, `metadata.json` |

### Cara menjalankan
1. Buka `notebook.ipynb` di Google Colab atau Jupyter.
2. Jalankan sel secara berurutan. Saat notebook dijalankan, hasil disimpan di folder `output/`, `output_multidaerah/`, dan `output_clean/`.
3. Scraping memakai jeda 2 detik per permintaan. Hasil pencarian Cookpad berubah dari waktu ke waktu, sehingga data pilot yang dipakai di proposal adalah `recipes_raw.json` di repositori ini.

### Etika dan lisensi
- Hanya judul resep dan nama bahan yang diambil. Nama penulis, foto, langkah memasak, dan komentar tidak dikumpulkan.
- Penggunaan untuk tugas akademik non-komersial. Rilis korpus final hanya memuat data agregat (nodes/edges).
- Dataset turunan: CC BY-NC 4.0. Kode: MIT.

### Cara mengutip
Kelompok 7 (2026). *Jaringan Ko-kemunculan Bahan Masakan Nusantara* [dataset]. https://github.com/gabrielaaku/sna-gastronomi-nusantara-kelompok7

## English

### Dataset summary
An undirected, weighted ingredient co-occurrence network built from Indonesian recipes. Nodes are ingredients. An edge links two ingredients that appear in the same recipe, and its weight is the number of recipes that contain the pair. The pilot (13–14 Nov 2026) covers 60 "rendang" recipes from Cookpad Indonesia (https://cookpad.com/id/cari/rendang), with 233 nodes and 2,343 edges. A test scrape of five dishes from other regions (gudeg, rawon, woku, ayam betutu, soto betawi; 10 recipes each) was added, and after ingredient-name normalization the combined data has 109 recipes, 97 ingredients and 1,751 edges.

### Files
| File | Contents |
|---|---|
| `recipes_raw.json` | Raw rendang recipes: url, title, and ingredient list |
| `nodes.csv` | `id, label` |
| `edges.csv` | `source, target, weight` |
| `notebook.ipynb` | Scraping, normalization, network construction, pilot statistics, and metadata |
| `recipes_multidaerah.json` | Test scrape of five dishes from other regions, 10 recipes each |
| `output_clean/` | Network after ingredient-name normalization: `nodes_clean.csv`, `edges_clean.csv`, `mapping_bahan.csv`, `ringkasan_normalisasi.csv`, `metadata.json` |

### Usage
1. Open `notebook.ipynb` in Google Colab or Jupyter.
2. Run the cells in order. When the notebook runs, outputs are written to `output/`, `output_multidaerah/`, and `output_clean/`.
3. Scraping uses a 2-second delay per request. Because Cookpad search results change over time, the pilot snapshot used in the proposal is the `recipes_raw.json` file in this repository.

### Ethics and license
- Only recipe titles and ingredient names are collected. Author names, photos, cooking steps and comments are not.
- For non-commercial academic use. The final corpus release contains only aggregated data (nodes/edges).
- Derived dataset: CC BY-NC 4.0. Code: MIT.

### Citation
Group 7 (2026). *Jaringan Ko-kemunculan Bahan Masakan Nusantara* (Nusantara Ingredient Co-occurrence Network) [dataset]. https://github.com/gabrielaaku/sna-gastronomi-nusantara-kelompok7
