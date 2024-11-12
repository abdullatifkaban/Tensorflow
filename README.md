
# GPU Destekli TensorFlow Kurulumu

**Nvidia Ekran Kartı** bulunan bilgisayarlar için **GPU destekli TensorFlow** kurulum rehberine hoş geldiniz!  
Aşağıda, belirli bir sistemde yapılan kurulum adımlarını bulacaksınız:

- **Ekran Kartı**: NVIDIA GeForce GTX 1650 Ti
- **İşletim Sistemi**: Linux Mint 22 Cinnamon 64bit

---

# Miniconda Kurulumu

1. **Miniconda**'yı indirerek başlayın. Kurulum dosyasını [buradan](https://www.anaconda.com/download/success) indirebilirsiniz.
2. Daha fazla bilgi ve kurulum adımları için [bu bağlantıyı](https://docs.anaconda.com/miniconda/miniconda-install/) inceleyebilirsiniz.

---

# Yeni Ortam Oluşturma

1. TensorFlow kullanımında yeni bir ortam oluşturmak için şu komutu kullanın:

```bash
conda create -n tensorflow python=3.12
```

2. Oluşturduğunuz ortamı aktifleştirmek için:

```bash
conda activate tensorflow
```

---

# TensorFlow Kurulumu

1. Öncelikle, `pip` paket yöneticinizi güncelleyin:

```bash
pip install --upgrade pip
```

2. GPU destekli TensorFlow kurulumunu başlatmak için:


```bash
pip install tensorflow[and-cuda]
```
> **İpucu**: Zsh terminalinde `tensorflow[and-cuda]` ifadesini tırnak içine almanız gerekmektedir.

**zsh:**
```zsh
pip install "tensorflow[and-cuda]"
```

3. Kurulumun başarılı olup olmadığını kontrol etmek için şu komutu çalıştırın:

```bash
python3 -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```

---

# Jupyter Notebook Kurulumu

1. Yeni oluşturduğunuz ortamda **Jupyter Notebook** kullanabilmek için ayrıca kurulum yapmalısınız:

```bash
pip install jupyter
```

2. **Jupyter Notebook** programını çalıştırmak için projenizin olduğu klasöre giderek aşağıdaki komutu çalıştırın:

```bash
jupyter notebook
```
---

Artık GPU destekli TensorFlow ve Jupyter Notebook ile çalışma ortamınızı başarıyla kurmuş olmalısınız! Herhangi bir sorunuz olursa, topluluk forumlarından veya ilgili belgelerden yardım alabilirsiniz.

Tensorflow kurulumu ile ilgili detaylı bilgiye [buradan](https://www.tensorflow.org/install/pip?hl=tr) ulaşabilirsiniz.