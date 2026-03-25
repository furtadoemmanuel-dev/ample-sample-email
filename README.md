# Ample.Sample — Email Marketing HTML

Template de email marketing profissional da **Ample.Sample**, pronto para envio via Hostinger Email, Gmail, Outlook ou qualquer plataforma SMTP.

---

## Estrutura do Repositório

```
ample-sample-email/
├── index.html     ← Template principal (pronto para uso)
└── README.md      ← Instruções de envio
```

---

## Como Enviar pelo Hostinger (Titan Mail / Webmail)

### Passo a passo — Webmail

1. Acesse [hpanel.hostinger.com](https://hpanel.hostinger.com) e faça login
2. Vá em **Emails** → clique em **Acessar Webmail** ao lado do email `contato@amplesample.solutions`
3. Clique em **Novo Email** (ícone de lápis / composição)
4. Preencha os campos:
   - **Para:** endereço(s) do(s) destinatário(s)
   - **Assunto sugerido:** `O encontro entre inovação e propósito — Ample.Sample`
5. No editor de texto, localize o ícone **`< >`** (Código-fonte / HTML)
6. **Apague todo o conteúdo** existente na caixa de código
7. **Cole o conteúdo completo** do arquivo `index.html`
8. Clique em **OK** ou **Aplicar**
9. Revise o preview visual e clique em **Enviar**

---

## Configurações SMTP do Hostinger

Para integrar com plataformas de disparo (Mailchimp, Brevo, RD Station etc.):

| Campo | Valor |
|---|---|
| **Host SMTP** | `smtp.hostinger.com` |
| **Porta SSL** | `465` |
| **Porta TLS** | `587` |
| **Usuário** | `contato@amplesample.solutions` |
| **Senha** | senha do email Hostinger |
| **Segurança** | SSL/TLS |

---

## Envio Programático via PHP (PHPMailer)

```php
<?php
use PHPMailer\PHPMailer\PHPMailer;

$mail = new PHPMailer(true);
$mail->isSMTP();
$mail->Host       = 'smtp.hostinger.com';
$mail->SMTPAuth   = true;
$mail->Username   = 'contato@amplesample.solutions';
$mail->Password   = 'SUA_SENHA';
$mail->SMTPSecure = 'ssl';
$mail->Port       = 465;
$mail->CharSet    = 'UTF-8';

$mail->setFrom('contato@amplesample.solutions', 'Ample.Sample');
$mail->addAddress('destinatario@email.com', 'Nome do Destinatário');

$mail->Subject = 'O encontro entre inovação e propósito — Ample.Sample';
$mail->isHTML(true);
$mail->Body    = file_get_contents(__DIR__ . '/index.html');

$mail->send();
echo 'Email enviado com sucesso.';
?>
```

---

## Imagens — CDN Pública

Todas as imagens estão hospedadas em CDN e carregam automaticamente. Nenhum upload adicional é necessário.

| Elemento | Arquivo |
|---|---|
| Logo branco (header e footer) | `IJLtkdDqCzsQkMrN.png` |
| Header — modelo editorial (IA) | `MgYGDRpPgkaSqgqX.jpg` |
| Imagem de equipe criativa | `FsHUnWJrjQebfpWq.jpg` |
| Thumbnail do vídeo YouTube | `YeJqYlFuSIqHkxta.jpg` |

---

## Antes de Enviar — Checklist

- [ ] Substituir `[UNSUBSCRIBE_LINK]` pelo link de descadastro real
- [ ] Confirmar o assunto do email
- [ ] Testar envio para um endereço próprio antes do disparo final
- [ ] Verificar visualização no mobile

---

## Compatibilidade

Compatível com Gmail, Outlook 2016/2019/365, Apple Mail, Titan Mail (Hostinger), Yahoo Mail e dispositivos móveis.

---

**Ample.Sample** — [amplesample.solutions](https://amplesample.solutions)  
contato@amplesample.solutions | CNPJ 57.864.015/0001-15
