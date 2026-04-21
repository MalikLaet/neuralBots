# NeuralBot — Site de Chatbots & Agentes de IA

Site de landing page completo, moderno e responsivo para venda de chatbots e agentes de IA.

---

## 🚀 Como rodar localmente

O projeto é um arquivo HTML único, sem dependências para instalar.

### Opção 1: Abrir direto no navegador
Apenas dê duplo clique no arquivo `index.html`.

### Opção 2: Servidor local (recomendado para evitar problemas de CORS)

**Com Python (já vem no sistema):**
```bash
# Python 3
python -m http.server 3000

# Depois acesse: http://localhost:3000
```

**Com Node.js (npx):**
```bash
npx serve .
# Acesse a URL exibida no terminal
```

**Com VS Code:**
Instale a extensão "Live Server" e clique em "Go Live" na barra inferior.

---

## ⚙️ Configuração rápida

Abra o arquivo `index.html` e localize o bloco de configuração do WhatsApp no JavaScript (linha ~450):

```javascript
const WHATSAPP_CONFIG = {
  number: "5511999999999",    // ← Substitua pelo seu número (com DDI+DDD, sem + ou espaços)
  message: "Olá! Vim pelo site e quero saber mais sobre os chatbots.",  // ← Mensagem inicial
};
```

**Exemplo real:**
```javascript
number: "5511987654321",   // DDI 55 + DDD 11 + número
```

---

## 📁 Estrutura do projeto

```
index.html          ← Arquivo principal (HTML + CSS + JS em um arquivo só)
README.md           ← Este arquivo
```

O site foi projetado como **single-file** para máxima portabilidade.
Para projetos maiores, separe em `style.css` e `main.js`.

---

## 🎨 Personalização

### Cores (CSS Variables — linha ~12 do `<style>`)
```css
--accent:   #00d4aa;   /* Verde-ciano principal */
--accent-2: #3b82f6;   /* Azul secundário */
```

### Textos
Busque pelos textos diretamente no HTML e substitua pelo conteúdo real do seu negócio:
- Nome da empresa: `NeuralBot`
- Número de projetos, taxas, etc. na seção Hero Stats
- Depoimento na seção Diferenciais
- E-mail no Footer

### Redes Sociais
Localize os links no `<footer>` com `aria-label="Instagram"`, `"LinkedIn"`, etc., e substitua o `href="#"` pela URL real.

---

## 📬 Integração com Backend (formulário)

O formulário está preparado para integração. Localize a função `handleFormSubmit` no JS e substitua o comentário pelo fetch real:

```javascript
fetch('/api/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(data),
}).then(r => r.json()).then(() => {
  // feedback de sucesso
});
```

---

## ☁️ Deploy / Hospedagem

### ✅ Vercel (recomendado — gratuito)
1. Crie conta em [vercel.com](https://vercel.com)
2. Instale a CLI: `npm i -g vercel`
3. Na pasta do projeto: `vercel deploy`
4. Pronto! Você receberá uma URL HTTPS.

### Netlify (alternativa gratuita)
1. Acesse [netlify.com](https://netlify.com)
2. Arraste a pasta do projeto para o painel de deploy
3. Site no ar em segundos.

### GitHub Pages (gratuito)
1. Suba o projeto em um repositório público no GitHub
2. Vá em Settings → Pages → selecione a branch `main`
3. URL disponível em `https://seuusuario.github.io/repositorio`

---

## 📦 Dependências externas (CDN)

O projeto usa apenas:
- **Google Fonts** — Syne + DM Sans (tipografia)
- **Lucide Icons** — ícones leves via CDN

Ambas são carregadas via CDN, sem necessidade de instalação.

---

## 📄 Seções do site

| Seção          | ID           | Descrição                              |
|----------------|--------------|----------------------------------------|
| Hero           | `#inicio`    | Título, subtítulo e CTA WhatsApp       |
| Sobre          | `#sobre`     | O que são chatbots + benefícios        |
| Serviços       | `#servicos`  | 6 cards de serviços oferecidos         |
| Diferenciais   | `#diferenciais` | Por que escolher + depoimento       |
| Contato        | `#contato`   | Botão WhatsApp + formulário            |
| Footer         | —            | Links, redes sociais, copyright        |

---

Feito com ❤️ — pronto para converter visitantes em clientes!
