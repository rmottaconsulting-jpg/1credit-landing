# 🚀 Landing Page 1CREDIT - Guia Completo de Instalação

## 📦 Arquivos Incluídos

- `index.html` - Landing page principal (página de vendas)
- `obrigado.html` - Página de agradecimento pós-compra (com botão WhatsApp)
- `README.md` - Este arquivo com instruções

---

## ⚡ Opção 1: Netlify (Recomendado - MAIS FÁCIL)

### Passo a Passo:

1. **Criar conta gratuita**
   - Acesse: https://www.netlify.com/
   - Clique em "Sign up" (pode usar conta do GitHub, GitLab ou email)

2. **Fazer upload dos arquivos**
   - Após login, clique em "Add new site" > "Deploy manually"
   - Arraste os arquivos `index.html` e `obrigado.html` para a área indicada
   - Aguarde o deploy (30 segundos)

3. **Seu site está no ar!**
   - Netlify vai gerar um endereço tipo: `https://seu-site-123abc.netlify.app`
   - Você pode mudar esse nome em: Site settings > Site details > Change site name

4. **Usar domínio próprio (opcional)**
   - Site settings > Domain management > Add custom domain
   - Digite seu domínio: `acesso1creditcompra.com.br`
   - Siga as instruções para configurar DNS

---

## 🔵 Opção 2: Vercel (Alternativa Rápida)

### Passo a Passo:

1. **Criar conta gratuita**
   - Acesse: https://vercel.com/
   - Clique em "Sign up" (pode usar GitHub ou email)

2. **Fazer upload**
   - Clique em "Add New..." > "Project"
   - Arraste os 2 arquivos HTML
   - Clique em "Deploy"

3. **Configurar domínio**
   - Settings > Domains
   - Adicione seu domínio personalizado

---

## 🟢 Opção 3: GitHub Pages (Grátis e Permanente)

### Se você não conhece Git, siga este método simples:

1. **Criar conta no GitHub**
   - Acesse: https://github.com/
   - Clique em "Sign up"

2. **Criar novo repositório**
   - Clique no "+" no canto superior direito
   - "New repository"
   - Nome: `1credit-landing`
   - Marque "Public"
   - Clique em "Create repository"

3. **Fazer upload dos arquivos**
   - Clique em "uploading an existing file"
   - Arraste `index.html` e `obrigado.html`
   - Clique em "Commit changes"

4. **Ativar GitHub Pages**
   - Vá em Settings > Pages
   - Em "Source", selecione "main" branch
   - Clique em "Save"
   - Seu site estará em: `https://seu-usuario.github.io/1credit-landing/`

---

## 🔗 Configurar na Kiwify

### Após hospedar, configure o redirecionamento:

1. **Acesse sua conta Kiwify**
   - Entre no produto que você está vendendo

2. **Configurar URL de retorno**
   - Vá em: **Configurações do Produto** ou **Checkout**
   - Procure por: **"URL de Agradecimento"** ou **"Página de Obrigado"**
   - Cole o link completo da sua página de obrigado:
   
   ```
   https://seu-site.netlify.app/obrigado.html
   ```
   
   OU se estiver usando domínio próprio:
   
   ```
   https://acesso1creditcompra.com.br/obrigado.html
   ```

3. **Salvar configurações**
   - Clique em "Salvar"
   - Faça um teste comprando o produto (use ambiente de teste da Kiwify se disponível)

---

## ✅ Testar o Fluxo Completo

### Simulação do cliente:

1. Cliente acessa: `https://seu-site.netlify.app/`
2. Cliente clica em "Fazer Diagnóstico" → vai para Kiwify
3. Cliente finaliza pagamento na Kiwify
4. Kiwify redireciona para: `https://seu-site.netlify.app/obrigado.html`
5. Cliente clica em "Falar com Especialista" → abre WhatsApp

**Link WhatsApp configurado:**
```
https://wa.me/5511235975512
```

---

## 📱 Personalizar WhatsApp

Se quiser mudar o número ou mensagem automática:

1. Abra `obrigado.html` em qualquer editor de texto
2. Procure por esta linha (por volta da linha 298):

```html
<a href="https://wa.me/5511235975512?text=Ol%C3%A1%21%20Acabei%20de%20fazer%20o%20pagamento..."
```

3. Substitua:
   - `5511235975512` → seu número no formato: `55DDDNUMERO` (sem espaços ou hífens)
   - Mensagem personalizada após `text=`

---

## 🎨 Personalizar Cores ou Textos

### Para mudar textos:

1. Abra os arquivos HTML em qualquer editor de texto (Notepad, VS Code, Sublime)
2. Procure pelo texto que quer mudar
3. Salve e faça upload novamente

### Para mudar cores:

No início de cada arquivo HTML, procure por:

```css
:root {
  --gold: #D4AF37;        /* Cor dourada principal */
  --gold-light: #F4D03F;  /* Dourado claro */
  --gold-dark: #B8941E;   /* Dourado escuro */
  --bg-dark: #0A0A0A;     /* Fundo preto */
}
```

Substitua os códigos de cor (ex: `#D4AF37`) pelos que você preferir.

---

## 🔥 Dicas de Conversão

### Para aumentar vendas:

1. **Teste A/B**: Crie 2 versões da landing page e veja qual converte mais
2. **Urgência**: Adicione contadores de tempo (escassez)
3. **Prova Social**: Adicione mais depoimentos reais
4. **Video**: O vídeo é crucial - garanta que ele carregue rápido
5. **Mobile**: 70% dos acessos vêm de celular - teste sempre no celular

### Métricas para acompanhar:

- Taxa de conversão (visitantes → compradores)
- Taxa de cliques no WhatsApp (após compra)
- Tempo médio na página
- Taxa de abandono

Use Google Analytics (gratuito) para rastrear tudo isso.

---

## ❓ Problemas Comuns

### "A página não está redirecionando da Kiwify"

**Solução:**
- Verifique se você colocou o link COMPLETO na Kiwify (com `https://`)
- Teste manualmente: abra o link `https://seu-site.com/obrigado.html` no navegador
- Limpe o cache do navegador (Ctrl + Shift + Delete)

### "O WhatsApp não abre"

**Solução:**
- Confirme que o número está no formato correto: `5511235975512`
- Não use espaços, parênteses ou hífens
- O número deve ter DDD + número completo com 9º dígito

### "Quero usar meu domínio próprio"

**Solução:**
- Compre um domínio no Registro.br ou Hostinger
- Configure os DNS apontando para Netlify/Vercel
- Na Netlify/Vercel, adicione o domínio personalizado
- Aguarde propagação DNS (até 24h)

---

## 📞 Suporte

Se precisar de ajuda:

1. Releia este README com calma
2. Assista tutoriais no YouTube sobre "Como hospedar site no Netlify"
3. Entre em contato com suporte da Netlify/Vercel (eles têm chat ao vivo)

---

## 🎉 Pronto!

Agora você tem:

✅ Landing page profissional hospedada
✅ Página de obrigado com WhatsApp
✅ Integração com Kiwify funcionando
✅ Controle total dos arquivos

**Boa sorte com suas vendas! 🚀💰**

---

## 📊 Próximos Passos Recomendados

1. Configurar Google Analytics
2. Instalar Pixel do Facebook/Meta
3. Criar anúncios direcionados
4. Testar diferentes headlines
5. Coletar depoimentos reais de clientes
6. Otimizar a página para SEO

---

**Última atualização:** Janeiro 2025  
**Desenvolvido para:** 1CREDIT  
**WhatsApp:** (11) 2359-7512