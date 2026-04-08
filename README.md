# 🚀 Release Notes Web

Sistema simples e moderno para exibir **notas de versão (changelog)** diretamente no navegador, com suporte a múltiplos projetos como:

* 🧾 PDV (Frente de Caixa)
* 📦 Retaguarda

Tudo carregado dinamicamente via arquivo JSON — sem precisar mexer no HTML.

---

## 📸 Preview

Interface estilo documentação moderna, com:

* Menu lateral
* Busca por texto
* Separação por projeto
* Destaque de versão mais recente (Latest)

---

## 📂 Estrutura do Projeto

```
/
  index.html
  releases.json
  /images
    logo.png
```

---

## ⚙️ Como funciona

O sistema carrega os dados a partir do arquivo:

```
releases.json
```

E renderiza automaticamente na tela.

---

## 🧠 Formato do JSON

```json
[
  {
    "project": "Retaguarda",
    "releases": [
      {
        "version": "2.0",
        "date": "Abril 2026",
        "changes": [
          { "type": "new", "text": "Nova funcionalidade" },
          { "type": "fix", "text": "Correção de bug" }
        ]
      }
    ]
  }
]
```

---

## 🏷️ Tipos de alterações

| Tipo      | Descrição           |
| --------- | ------------------- |
| `new`     | Nova funcionalidade |
| `fix`     | Correção de erro    |
| `improve` | Melhoria geral      |

---

## 🌐 Publicação no GitHub Pages

1. Suba os arquivos no repositório
2. Vá em **Settings > Pages**
3. Configure:

   ```
   Branch: main
   Folder: / (root)
   ```
4. Acesse:

```
https://seu-usuario.github.io/seu-repo/
```

---

## ⚠️ Problemas comuns

### ❌ Erro ao carregar `releases.json`

Possíveis causas:

* Arquivo não está na mesma pasta do `index.html`
* Nome errado (`Releases.json` ≠ `releases.json`)
* JSON inválido
* Caminho incorreto no `fetch()`

Teste direto no navegador:

```
https://seu-site/releases.json
```

---

## 🛠️ Desenvolvimento local

Evite abrir o HTML diretamente (`file://`)

Use um servidor local:

### VS Code (recomendado)

* Instale extensão **Live Server**
* Clique em "Open with Live Server"

---

## 🚀 Próximas melhorias

* [ ] Menu colapsável por projeto
* [ ] Filtro por tipo (fix, new, improve)
* [ ] Tema claro/escuro
* [ ] Destaque de última versão global
* [ ] Integração com API

---

## 📄 Licença

Projeto livre para uso interno e personalização.

---

## 💡 Autor

Desenvolvido para organização de releases de sistemas PDV e Retaguarda.
