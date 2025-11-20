# 🚀 GUIA COMPLETO - GitHub Actions

## 📋 O que foi criado

Criei uma automação que gera o APK **automaticamente** toda vez que você fizer upload no GitHub!

### ✅ Arquivos criados:
- `.github/workflows/build-apk.yml` - Configuração da automação
- `README.md` - Documentação do projeto

---

## 🎯 PASSO A PASSO COMPLETO

### 1️⃣ Criar Repositório no GitHub

1. Acesse: https://github.com/new
2. Nome do repositório: `tem-tudo-caixa` (ou outro nome)
3. Marque: **Public** (para usar GitHub Actions grátis)
4. Clique em: **Create repository**

---

### 2️⃣ Enviar seus arquivos para o GitHub

**OPÇÃO A - Usando GitHub Desktop (Mais Fácil):**

1. Baixe: https://desktop.github.com
2. Instale e faça login
3. Clique em: **Add** → **Add existing repository**
4. Selecione a pasta: `C:\Users\pedro\OneDrive\Documentos\Vendas`
5. Clique em: **Publish repository**
6. Pronto! ✅

**OPÇÃO B - Usando linha de comando:**

Abra o PowerShell na pasta do projeto e execute:

```powershell
cd "C:\Users\pedro\OneDrive\Documentos\Vendas"

# Inicializar git (se ainda não tiver)
git init

# Adicionar todos os arquivos
git add .

# Fazer commit
git commit -m "Primeiro commit - Tem Tudo 1.99"

# Conectar ao GitHub (substitua SEU_USUARIO e SEU_REPOSITORIO)
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/tem-tudo-caixa.git

# Enviar para o GitHub
git push -u origin main
```

---

### 3️⃣ Aguardar a Compilação Automática

Depois do push, automaticamente:

1. GitHub Actions inicia a compilação
2. Instala todas as dependências
3. Gera o APK
4. Disponibiliza para download

**Tempo:** ~20 minutos

---

### 4️⃣ Baixar o APK Gerado

1. Vá no seu repositório no GitHub
2. Clique na aba **Actions** (no topo)
3. Clique no workflow **"Build APK Android"** mais recente
4. Role até o final da página
5. Em **Artifacts**, clique em **temtudo-apk**
6. Baixa um ZIP com o APK dentro
7. Extraia e transfira para o celular

---

## 🔄 ATUALIZAR O APP (Próximas vezes)

Toda vez que você quiser atualizar o app:

### Usando GitHub Desktop:
1. Abra o GitHub Desktop
2. Modifique os arquivos (main.py, etc)
3. GitHub Desktop mostra as mudanças
4. Digite uma mensagem: "Melhorias no app"
5. Clique em **Commit to main**
6. Clique em **Push origin**
7. **Pronto!** GitHub compila automaticamente

### Usando linha de comando:
```powershell
cd "C:\Users\pedro\OneDrive\Documentos\Vendas"
git add .
git commit -m "Descrição da mudança"
git push
```

---

## 📱 INSTALAR NO CELULAR

1. Baixe o ZIP do APK do GitHub
2. Extraia o arquivo `.apk`
3. Transfira para o celular (WhatsApp, cabo USB, etc)
4. No celular, abra o arquivo APK
5. Permita "Instalar de fontes desconhecidas"
6. Clique em **Instalar**
7. Pronto! ✅

---

## ❓ PERGUNTAS FREQUENTES

### "Não tenho GitHub"
Crie grátis em: https://github.com/signup

### "GitHub Actions é grátis?"
✅ Sim! Para repositórios públicos é 100% grátis

### "Posso usar repositório privado?"
Sim, mas tem limite de minutos grátis por mês

### "Como ver se está compilando?"
Vá em **Actions** no GitHub. Se tiver um círculo amarelo ⚪, está compilando.
Se tiver ✅ verde, compilou com sucesso!

### "Deu erro na compilação"
Clique no workflow com erro (❌ vermelho) para ver os logs.
Geralmente é problema no `buildozer.spec`.

### "Quanto tempo demora?"
~20 minutos para compilar. Mas é automático, não precisa fazer nada!

---

## 🎉 VANTAGENS DO GITHUB ACTIONS

✅ **100% Automático** - Só fazer push
✅ **Grátis** - Para repositórios públicos
✅ **Rápido** - 20 minutos
✅ **Sempre disponível** - Não depende do seu PC
✅ **Histórico** - Guarda todas as versões compiladas
✅ **Profissional** - Usado por grandes empresas

---

## 🔧 COMANDOS ÚTEIS

### Ver status do repositório:
```powershell
git status
```

### Ver histórico de commits:
```powershell
git log --oneline
```

### Desfazer mudanças (antes do commit):
```powershell
git checkout -- .
```

### Ver diferenças:
```powershell
git diff
```

---

## 📞 PRONTO PARA COMEÇAR?

1. ✅ Arquivos criados
2. ⏳ Criar repositório no GitHub
3. ⏳ Fazer push dos arquivos
4. ⏳ Aguardar compilação
5. ⏳ Baixar APK

**Próximo passo:** Criar o repositório no GitHub! 🚀
