# Ganimedes.ai - Configuração de Domínio

> Documentação completa da configuração do domínio ganimedes.ai
> Última atualização: 2026-01-06

---

## 📋 Informações Gerais

| Item | Valor |
|------|-------|
| **Domínio Principal** | ganimedes.ai |
| **Domínio com WWW** | www.ganimedes.ai |
| **Plataforma de Hospedagem** | Cloudflare Pages |
| **Canonical URL** | https://ganimedes.ai/ |
| **Status** | ✅ Ativo e Funcionando |

---

## 🌐 Configuração DNS (Cloudflare)

### Registros DNS Configurados:

| Tipo | Nome | Conteúdo | Proxy | TTL |
|------|------|----------|-------|-----|
| **CNAME** | ganimedes.ai | ganimedes.pages.dev | ✅ Proxied | Auto |
| **CNAME** | www | ganimedes.pages.dev | ✅ Proxied | Auto |
| **MX** | @ | route1.mx.cloudflare.net (78) | ❌ DNS only | Auto |
| **MX** | @ | route2.mx.cloudflare.net (99) | ❌ DNS only | Auto |
| **MX** | @ | route3.mx.cloudflare.net (55) | ❌ DNS only | Auto |
| **TXT** | @ | v=spf1 include:_spf.mx.cloudflare.net include:spf.brevo.com ~all | ❌ DNS only | Auto |
| **TXT** | _dmarc | v=DMARC1; p=none; rua=mailto:rua@dmarc.brevo.com | ❌ DNS only | 1 hr |
| **TXT** | @ | google-site-verification=... | ❌ DNS only | 1 hr |
| **TXT** | @ | brevo-code:... | ❌ DNS only | 1 hr |
| **CNAME** | cf2024-1._domainkey | [DKIM record Cloudflare] | ❌ DNS only | Auto |
| **CNAME** | brevo1._domainkey | b1.ganimedes-ai.dkim.brevo.com | ❌ DNS only | 1 hr |
| **CNAME** | brevo2._domainkey | b2.ganimedes-ai.dkim.brevo.com | ❌ DNS only | 1 hr |

**Total de Registros DNS**: 12

---

## 🚀 Cloudflare Pages - Custom Domains

### Domínios Configurados:

| Domínio | Status | SSL | Configuração |
|---------|--------|-----|--------------|
| **ganimedes.ai** | ✅ Active | ✅ Enabled | Domínio principal |
| **www.ganimedes.ai** | ✅ Active | ✅ Enabled | Subdomínio www |

### URL do Projeto Pages:
- `ganimedes.pages.dev`

---

## 📄 SEO e Indexação

### Sitemap
- **URL**: https://ganimedes.ai/sitemap.xml
- **Última modificação**: 2026-01-06
- **Frequência de atualização**: monthly
- **Prioridade**: 1.0

### Tag Canonical
```html
<link rel="canonical" href="https://ganimedes.ai/">
```

### Meta Tags SEO
```html
<title>Ganimedes.ai - Inteligência Artificial | Next Level AI Solutions</title>
<meta name="description" content="Ganimedes.ai - Soluções avançadas em Inteligência Artificial. Next Level. Beyond Orbits. Beyond Limits. Transforme seu negócio com IA de ponta.">
<meta name="keywords" content="inteligência artificial, AI, machine learning, deep learning, automação, tecnologia, inovação, ganimedes, soluções AI">
```

### Google Search Console
- **Propriedade**: sc-domain:ganimedes.ai
- **Status de Indexação**: ✅ URLs indexados
- **Última solicitação de indexação**: 2026-01-06
  - https://ganimedes.ai/ - ✅ Indexado
  - https://www.ganimedes.ai/ - ✅ Indexação solicitada

### Analytics
- **Google Analytics 4**: G-FHE45YQFKF

---

## 📧 Configuração de Email (Cloudflare Email Routing + Brevo)

### Provedor de Email:
- **Serviço Principal**: Cloudflare Email Routing
- **Serviço SMTP**: Brevo (para envio)

### Registros DNS de Email:
- ✅ MX records configurados (Cloudflare)
- ✅ SPF configurado (Cloudflare + Brevo)
- ✅ DMARC configurado (com reporting para Brevo)
- ✅ DKIM configurado (Cloudflare + Brevo dual-signing)

### Email de Contato:
- **info@ganimedes.ai** - Email de contato exibido no site

---

## ✅ Status de Verificação

### Testes Realizados (2026-01-06):

| Teste | Status | Observações |
|-------|--------|-------------|
| **DNS CNAME www** | ✅ Pass | Registro configurado corretamente |
| **Custom Domain Pages** | ✅ Pass | Ativo com SSL habilitado |
| **Acesso via www.ganimedes.ai** | ✅ Pass | Site carrega corretamente |
| **Acesso via ganimedes.ai** | ✅ Pass | Site carrega corretamente |
| **Redirecionamento HTTPS** | ✅ Pass | Automático via Cloudflare |
| **SSL/TLS** | ✅ Pass | Certificado válido |
| **Sitemap acessível** | ✅ Pass | https://ganimedes.ai/sitemap.xml |
| **Google Search Console** | ✅ Pass | Indexação solicitada com sucesso |
| **Google Analytics** | ✅ Pass | GA4 configurado e funcionando |

---

## 🔧 Resolução de Problemas

### Problema Original:
**Google Search Console** reportou erro de redirecionamento para www.ganimedes.ai

### Causa Raiz:
- CNAME DNS `www` estava configurado previamente
- Custom Domain `www.ganimedes.ai` já estava registrado no Cloudflare Pages
- Apenas sitemap.xml precisava ser atualizado

### Solução Implementada:
1. ✅ Verificado CNAME `www → ganimedes.pages.dev` no DNS Cloudflare (já existia)
2. ✅ Verificado `www.ganimedes.ai` como Custom Domain no Cloudflare Pages (já ativo)
3. ✅ Atualizado sitemap.xml com data 2026-01-06
4. ✅ Solicitada re-indexação no Google Search Console

### Data da Correção:
**2026-01-06**

---

## 📊 Informações Técnicas

### Cloudflare Account ID:
```
869651ccbc0e109d72a363c9ca7a0aa5
```

### Zone ID (ganimedes.ai):
```
97f3b4a60b1a24fa9d40bea51616e299
```

### Nameservers Cloudflare:
- `drake.ns.cloudflare.com`
- `rosalie.ns.cloudflare.com`

---

## 🎨 Características do Site

### Design:
- Landing page moderna com tema espacial
- Cores: Azul escuro (#050a12) e acentos azul brilhante
- Tema: "Next Level. Beyond Orbits. Beyond Limits."

### Tecnologias:
- HTML5 puro (sem frameworks)
- CSS3 com animações
- Google Analytics 4
- Cloudflare Pages (CDN global)

### Performance:
- **Visitantes únicos (24h)**: 63
- **Total de requisições (24h)**: 157
- **Cache**: 74.75%
- **Dados servidos (24h)**: 132 MB

---

## 📝 Histórico de Alterações

| Data | Alteração | Responsável |
|------|-----------|-------------|
| 2026-01-02 | Configuração inicial do domínio | Claude Code |
| 2026-01-02 | Configuração email Brevo + DKIM | Claude Code |
| 2026-01-06 | Verificação www: DNS CNAME + Custom Domain | Claude Code |
| 2026-01-06 | Atualização sitemap lastmod | Claude Code |
| 2026-01-06 | Solicitação indexação Google | Claude Code |

---

## 🔗 Links Úteis

- **Site Principal**: https://ganimedes.ai
- **Site com WWW**: https://www.ganimedes.ai
- **Sitemap**: https://ganimedes.ai/sitemap.xml
- **Cloudflare Dashboard**: https://dash.cloudflare.com/869651ccbc0e109d72a363c9ca7a0aa5/ganimedes.ai
- **Cloudflare Pages**: https://dash.cloudflare.com/869651ccbc0e109d72a363c9ca7a0aa5/pages/view/ganimedes
- **Google Search Console**: https://search.google.com/search-console?resource_id=sc-domain:ganimedes.ai

---

## ⚠️ Notas Importantes

1. **Canonical URL**: Sempre usar `https://ganimedes.ai/` (sem www) como canonical
2. **Redirecionamento**: www.ganimedes.ai funciona mas canonical aponta para versão sem www
3. **DNS Propagação**: Alterações DNS podem levar até 48h para propagar globalmente
4. **Indexação Google**: Solicitações de indexação são processadas em fila prioritária
5. **Email Brevo**: Configuração dual-DKIM (Cloudflare + Brevo) para melhor deliverability
6. **Analytics**: Dados disponíveis em tempo real no Google Analytics 4

---

**Documentação gerada automaticamente por Claude Code**
