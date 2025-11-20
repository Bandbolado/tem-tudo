# Instruções de Instalação e Execução - TemTudo 199

## 🖥️ Para Testar no Windows (Computador)

### 1. Instalar Python
- Baixe Python 3.8+ de https://www.python.org/downloads/
- Marque "Add Python to PATH" durante instalação

### 2. Instalar Dependências
Abra o PowerShell na pasta do projeto e execute:

```powershell
pip install kivy[base] kivy-examples
```

### 3. Executar o App
```powershell
python main.py
```

---

## 📱 Para Gerar APK Android (Use Google Colab)

Como o Buildozer não funciona no Windows, use o Google Colab:

### Passos no Google Colab:

1. Acesse: https://colab.research.google.com
2. Crie um novo notebook
3. Cole e execute estas células:

#### Célula 1 - Upload dos Arquivos
```python
from google.colab import files
import os

# Criar pasta do projeto
os.makedirs('TemTudo199', exist_ok=True)
os.chdir('TemTudo199')

# Upload dos arquivos
print("📤 Faça upload de: main.py, temtudo.kv, buildozer.spec")
uploaded = files.upload()
```

#### Célula 2 - Instalar Dependências
```python
!pip install buildozer cython==0.29.33
!sudo apt-get update
!sudo apt-get install -y \
    python3-pip \
    build-essential \
    git \
    python3-numpy \
    libsdl2-dev \
    libsdl2-image-dev \
    libsdl2-mixer-dev \
    libsdl2-ttf-dev \
    libportmidi-dev \
    libswscale-dev \
    libavformat-dev \
    libavcodec-dev \
    zlib1g-dev \
    libgstreamer1.0-dev \
    gstreamer1.0-plugins-base \
    libltdl-dev \
    openjdk-17-jdk \
    unzip \
    autoconf \
    libtool \
    automake
```

#### Célula 3 - Gerar APK
```python
# Limpar builds anteriores
!rm -rf .buildozer bin

# Gerar APK (demora 15-20 minutos)
!buildozer -v android debug

# Download do APK
from google.colab import files
import os

# Encontrar o APK
apk_files = !find bin -name "*.apk"
if apk_files:
    apk_path = apk_files[0]
    print(f"✅ APK gerado: {apk_path}")
    files.download(apk_path)
else:
    print("❌ Nenhum APK encontrado")
```

---

## 🎨 Funcionalidades do App

✅ **Nova Venda** - Registre produtos e valores  
✅ **Histórico** - Visualize todas as vendas  
✅ **Calculadoras** - Desconto e margem de lucro  
✅ **Interface Moderna** - Design profissional dark theme  
✅ **Dados Salvos** - Histórico persistente em JSON  

---

## 📋 Arquivos do Projeto

- `main.py` - Código principal do app
- `temtudo.kv` - Interface visual (design)
- `buildozer.spec` - Configuração para Android
- `historico.json` - Dados salvos (criado automaticamente)

---

## 🆘 Problemas Comuns

### "Buildozer não funciona no Windows"
✅ **Solução:** Use Google Colab (veja instruções acima)

### "Erro ao instalar Kivy"
✅ **Solução:** Execute `pip install --upgrade pip` primeiro

### "App não abre"
✅ **Solução:** Verifique se Python 3.8+ está instalado

---

## 📱 Testado em:
- Windows 10/11 (modo desktop)
- Android 5.1+ (via APK)
- Google Colab (para build)
