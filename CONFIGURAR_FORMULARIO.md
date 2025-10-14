# 📧 Como Configurar o Formulário de Contato

## 🔥 OPÇÃO 1: Formspree (RECOMENDADO - Grátis e Fácil)

### Passo 1: Criar conta no Formspree
1. Acesse: https://formspree.io/
2. Clique em "Get Started" 
3. Crie uma conta gratuita com seu email

### Passo 2: Criar um novo formulário
1. Após fazer login, clique em "+ New Form"
2. Digite um nome como "Site EMdA - Contato"
3. Copie o **Form ID** que será gerado (algo como `xpzgkdny`)

### Passo 3: Atualizar o site
1. No arquivo `index.html`, linha ~1225, troque:
   ```html
   <form class="contact-form" action="https://formspree.io/f/SEU_FORM_ID" method="POST">
   ```
   
   Por:
   ```html
   <form class="contact-form" action="https://formspree.io/f/xpzgkdny" method="POST">
   ```
   (substitua `xpzgkdny` pelo seu Form ID real)

### Passo 4: Fazer commit e push
```bash
git add .
git commit -m "✉️ Configurar formulário de contato com Formspree"
git push origin main
```

### Passo 5: Testar
- Aguarde o GitHub Pages atualizar (2-5 minutos)
- Acesse seu site e teste o formulário
- As mensagens chegará no seu email!

---

## 🔥 OPÇÃO 2: Netlify Forms (Se hospedar no Netlify)

Se você quiser migrar para o Netlify (também grátis):

1. Adicione `netlify` ao form:
   ```html
   <form class="contact-form" netlify>
   ```

2. Faça deploy no Netlify conectando seu repositório GitHub

---

## 🔥 OPÇÃO 3: EmailJS (Mais avançado)

Para enviar emails diretamente do JavaScript:

1. Crie conta em: https://www.emailjs.com/
2. Configure um serviço de email (Gmail, Outlook, etc.)
3. Substitua o JavaScript do formulário

---

## 📋 Características do Formspree (Plano Grátis):
- ✅ 50 submissões por mês
- ✅ Emails automáticos para você
- ✅ Spam protection
- ✅ Fácil configuração
- ✅ Funciona com GitHub Pages

## 📧 O que você receberá:
Quando alguém enviar uma mensagem, você receberá um email como:

```
De: noreply@formspree.io
Assunto: New submission from Contact Form

Nome: João Silva
Email: joao@email.com
Telefone: (11) 99999-9999
Mensagem: Gostaria de saber mais sobre o sistema PDV...
```

## 🚀 Próximos Passos:
1. Siga o Passo 1-3 acima
2. Atualize o código
3. Faça commit e push
4. Teste o formulário!

Precisa de ajuda? Me avise! 😊