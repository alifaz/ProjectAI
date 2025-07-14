# Text To Image & Video

Repository ini berisikan script Python yang menerima masukan (_prompt_) berupa teks dan mengubahnya menjadi file gambar dan video.

## Installation

Untuk menjalankan script Python ini dapat menggunakan Jupyter Notebook, PyCharm atau Visual Studio Code.
Lalu install library yang dibutuhkan dengan menggunakan package manager ```pip```.

### Text To Image

```bash
pip install torch diffusers transformers pillow
```

Line di atas untuk instalasi library berkaitan dengan model LLM, yaitu ```torch```, ```diffusers``` dan ```transformers``` dari Hugging Face, dan ```pillow``` yang merupakan library untuk
pemrosesan gambar dengan bahasa Python. Instalasi keempat library ini akan memakan waktu yang cukup lama karena besarnya model, begitupun saat menjalankan script nanti. Sehingga disarankan untuk menggunakan komputer yang memanfaatkan GPU, sebagai contoh environment CUDA yang dikembangkan oleh NVIDIA.

```bash
pip install accelerate
```

Line di atas untuk instalasi library ```accelerate``` yang dapat mempercepat proses inferensi, yaitu saat model LLM menjalankan proses pencarian/pengumpulan informasi berkaitan dengan _prompt_ yang diberikan pengguna.

### Text To Video

```bash
pip install imageio[ffmpeg]
```

Line di atas untuk instalasi library ```imageio``` dengan ekstensi MPEG/MP4 sehingga script dapat menghasilkan output berupa video dengan ekstensi MP4.

### Optional

```bash
pip install deep_translator
```

Untuk instalasi library ```deep_translator``` sehingga model dapat menerima masukan dalam bahasa non-Inggris (contoh: Indonesia)

```bash
pip install matplotlib
```

Untuk instalasi library ```matplotlib``` yang mendukung plotting gambar dan visualisasi gambar lebih lanjut (seperti scatter box dan histogram).

```bash
pip install tqdm
```

Untuk instalasi library ```tqdm``` yang dapat menampilkan progress bar saat proses inferensi/running model dan generasi gambar/video.


## Restriction

Model LLM, sebagaimana kita ketahui saat ini dilatih secara mayoritas dengan bahasa Inggris. Sehingga jika model tersebut diberikan _prompt_ dalam bahasa selain Inggris, keluaran yang diberikan dapat tidak akurat. Oleh karena itu _workaround_ yang dilakukan adalah dengan library '''deep_translator''' sehingga model tetap menerima _prompt_ dalam bahasa Inggris.

## License

[MIT](https://choosealicense.com/licenses/mit/)
