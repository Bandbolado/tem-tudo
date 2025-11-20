# Tem Tudo 1.99 - Sistema de Caixa

Sistema completo de caixa para comércio com geração automática de APK.

## 📱 Funcionalidades

- ✅ Registro de vendas
- ✅ Controle de estoque
- ✅ Histórico de vendas e orçamentos
- ✅ Geração de recibos
- ✅ Cálculo automático de troco
- ✅ Dados de entrega
- ✅ Interface amigável

## 🚀 Como gerar o APK

### Método Automático (GitHub Actions)

1. **Faça commit e push dos arquivos:**
   ```bash
   git add .
   git commit -m "Atualizar app"
   git push
   ```

2. **Aguarde a compilação:**
   - Vá em **Actions** no GitHub
   - Clique no workflow **"Build APK Android"**
   - Aguarde ~20 minutos

3. **Baixe o APK:**
   - No workflow concluído, clique em **Artifacts**
   - Baixe **"temtudo-apk"**
   - Extraia o ZIP e transfira o APK para o celular

### Método Manual (Google Colab)

Veja instruções detalhadas em: [GERAR_APK.md](GERAR_APK.md)

## 📦 Arquivos do Projeto

- `main.py` - Código principal do aplicativo
- `buildozer.spec` - Configuração para Android
- `.github/workflows/build-apk.yml` - Automação GitHub Actions

## 🔧 Executar localmente (Windows)

```bash
pip install kivy[base]
python main.py
```

## 📱 Instalar no Android

1. Transfira o APK para o celular
2. Permita "Instalar de fontes desconhecidas"
3. Instale o APK
4. Pronto!

## 📞 Dados da Empresa

- **Nome:** Tem Tudo 1.99
- **Endereço:** Rua Itapiru 543
- **Telefone:** (21) 96602-0453
- **CNPJ:** 50.785.469/0001-51

## 📄 Licença

Proprietário - Uso interno
