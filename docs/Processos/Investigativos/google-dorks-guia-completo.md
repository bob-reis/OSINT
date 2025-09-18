# Google Dorks — Guia Completo para OSINT

> **Aviso Ético**: Este conteúdo é destinado exclusivamente para fins defensivos, educacionais e de pesquisa autorizada. Use apenas em domínios próprios ou com autorização explícita. Respeite leis locais e Termos de Serviço.

## 📖 Índice

- [Introdução](#introdução)
- [Operadores Básicos](#operadores-básicos)
- [Operadores Avançados](#operadores-avançados)
- [Categorias de Dorks](#categorias-de-dorks)
  - [Arquivos de Configuração](#1-arquivos-de-configuração)
  - [Backups e Bancos de Dados](#2-backups-e-bancos-de-dados)
  - [Documentos Sensíveis](#3-documentos-sensíveis)
  - [Painéis Administrativos](#4-painéis-administrativos)
  - [APIs e Endpoints](#5-apis-e-endpoints)
  - [CMS Específicos](#6-cms-específicos)
  - [Credenciais e Secrets](#7-credenciais-e-secrets)
- [Casos de Uso Práticos](#casos-de-uso-práticos)
- [Proteção e Mitigação](#proteção-e-mitigação)
- [OPSEC para Investigadores](#opsec-para-investigadores)

---

## Introdução

Google Dorks (ou Google Hacking) são consultas de busca avançadas que utilizam operadores especiais para encontrar informações específicas indexadas pelos mecanismos de busca. Para analistas OSINT, são ferramentas poderosas para descobrir:

- Arquivos de configuração expostos
- Documentos confidenciais vazados
- Painéis administrativos desprotegidos
- Credenciais e secrets em repositórios públicos
- Vulnerabilidades em aplicações web

---

## Operadores Básicos

### 🔍 Filtros de Busca

| Operador | Descrição | Exemplo |
|----------|-----------|---------|
| `site:` | Busca apenas em um domínio específico | `site:example.com` |
| `filetype:` | Busca por tipo de arquivo | `filetype:pdf` |
| `ext:` | Sinônimo de filetype | `ext:log` |
| `inurl:` | Termo deve aparecer na URL | `inurl:admin` |
| `intitle:` | Termo deve aparecer no título | `intitle:"index of"` |
| `intext:` | Termo deve aparecer no conteúdo | `intext:password` |
| `cache:` | Mostra versão em cache | `cache:example.com` |
| `related:` | Sites similares | `related:github.com` |

### 🔗 Operadores Lógicos

| Operador | Descrição | Exemplo |
|----------|-----------|---------|
| `"termo"` | Busca exata (aspas) | `"login panel"` |
| `OR` ou `\|` | Operador OU | `site:github.com \| site:gitlab.com` |
| `AND` ou `&` | Operador E | `inurl:admin & intext:password` |
| `+` | Incluir termo obrigatório | `+password` |
| `-` | Excluir termo | `-site:wikipedia.org` |
| `*` | Wildcard/coringa | `site:*.example.com` |
| `()` | Agrupamento | `(site:github.com \| site:gitlab.com) intext:api_key` |

---

## Operadores Avançados

### 📅 Filtros Temporais
```
# Buscar arquivos criados em período específico
filetype:pdf (before:2024-01-01 after:2023-01-01)

# Combinar com outros filtros
site:example.com filetype:log before:2024-06-01
```

### 🔢 Filtros Numéricos
```
# Buscar números em faixas específicas
numrange:1000-9999

# Exemplo: buscar portas em configs
intext:"port" numrange:8000-9000 filetype:conf
```

### 🌐 Subdomínios
```
# Encontrar subdomínios
site:*.example.com

# Múltiplos níveis
site:*.*.example.com

# Excluir domínio principal
site:*.example.com -site:example.com
```

---

## Categorias de Dorks

### 1. 📄 Arquivos de Configuração

**Dorks básicos:**
```
# Configurações gerais
intitle:"index of" inurl:conf
filetype:conf password
inurl:config.php dbpasswd

# Arquivos específicos
inurl:wp-config.php intext:DB_PASSWORD
inurl:.env intext:API_KEY
filetype:ini intext:password

# Configurações de servidores
inurl:httpd.conf
inurl:nginx.conf
inurl:apache.conf
```

**Dorks avançados:**
```
# Combinações para maior precisão
site:*.com (inurl:config | inurl:conf) (intext:password | intext:secret)

# Arquivos de ambiente
filetype:env intext:SECRET_KEY
inurl:config intext:database password host

# Configurações em formato específico
filetype:yaml intext:password
filetype:json intext:secret
filetype:toml intext:password
```

### 2. 💾 Backups e Bancos de Dados

**Backups expostos:**
```
# Arquivos de backup
inurl:backup.zip
inurl:backup.sql
inurl:backup.tar.gz
filetype:bak

# Diretórios de backup
intitle:"index of" backup
inurl:backup "Parent Directory"
inurl:backups filetype:sql
```

**Bancos de dados:**
```
# Dumps de SQL
filetype:sql intext:INSERT
filetype:sql "CREATE TABLE"
inurl:dump.sql
inurl:database.sql

# Bancos específicos
filetype:sql intext:mysql
filetype:mdb
filetype:db
```

### 3. 📋 Documentos Sensíveis

**Documentos com informações confidenciais:**
```
# Documentos com termo "confidencial"
filetype:pdf intext:"confidencial"
filetype:docx intext:"confidencial"

# Documentos financeiros
filetype:xls intext:budget
filetype:xlsx intext:salary
filetype:csv intext:payment

# Documentos técnicos
filetype:pdf intext:"internal use only"
filetype:doc intext:"not for distribution"
```

**Logs expostos:**
```
# Logs de sistema
filetype:log
inurl:log intext:error
inurl:error.log

# Logs específicos
inurl:access.log
inurl:debug.log
filetype:log intext:password
```

### 4. 🔐 Painéis Administrativos

**Interfaces de administração:**
```
# Painéis genéricos
inurl:admin
intitle:"Admin Panel"
intitle:"Administrative Login"
inurl:admin/login

# Interfaces específicas
inurl:admin.php
inurl:administrator
inurl:controlpanel
inurl:cpanel
```

**Páginas de login:**
```
# Login genérico
intitle:"Login" inurl:login
intext:"username" intext:"password" inurl:login

# CMS específicos
inurl:wp-admin
inurl:administrator/index.php
inurl:/drupal/user/login
```

### 5. 🌐 APIs e Endpoints

**APIs expostas:**
```
# Endpoints de API
inurl:api
inurl:/v1/
inurl:/v2/
inurl:/api/v1/

# Documentação de API
intitle:"API Documentation"
inurl:swagger
inurl:api-docs
```

**Combinações efetivas:**
```
# API com parâmetros sensíveis
site:*.com inurl:api (intext:key | intext:token | intext:secret)

# REST APIs
inurl:/rest/
site:*/graphql
inurl:api.php
```

### 6. 🛠️ CMS Específicos

**WordPress:**
```
# Arquivos de configuração
inurl:wp-config.php intext:DB_PASSWORD
intitle:"Index of" wp-content
inurl:wp-content/uploads/

# Plugins vulneráveis
inurl:/wp-content/plugins/
inurl:wp-admin/admin-ajax.php
```

**Joomla:**
```
# Configurações Joomla
inurl:configuration.php intext:password
intitle:"Index of" administrator
inurl:/administrator/index.php
```

**Drupal:**
```
# Sites Drupal
inurl:user/login "Drupal"
inurl:/?q=admin
inurl:/drupal/
```

### 7. 🔑 Credenciais e Secrets

**API Keys e Tokens:**
```
# AWS Keys
intext:aws_access_key_id
intext:aws_secret_access_key
intext:AWS_SESSION_TOKEN

# GitHub Tokens
intext:github_token
intext:GITHUB_ACCESS_TOKEN

# API Keys genéricas
intext:api_key
intext:API_SECRET
intext:secret_key
```

**Senhas em repositórios:**
```
# Senhas em código
site:github.com intext:password
site:gitlab.com intext:secret
site:pastebin.com intext:password

# Credenciais de banco
intext:mysql password
intext:postgresql password
intext:"connection string" password
```

---

## Casos de Uso Práticos

### 🎯 Exemplo 1: Auditoria de Segurança Própria

**Objetivo**: Verificar exposições no domínio da empresa

```bash
# 1. Buscar arquivos de configuração expostos
site:example.com (ext:conf | ext:config | ext:ini | ext:env)

# 2. Verificar backups esquecidos
site:example.com (inurl:backup | inurl:bak | ext:backup | ext:old)

# 3. Localizar painéis admin desprotegidos
site:example.com (inurl:admin | inurl:administrator | intitle:"admin panel")

# 4. Buscar logs com informações sensíveis
site:example.com ext:log intext:password

# 5. Verificar documentos confidenciais
site:example.com (ext:pdf | ext:doc | ext:xlsx) intext:confidencial
```

### 🎯 Exemplo 2: Reconhecimento para Pentest Autorizado

**Objetivo**: Mapear superficie de ataque do cliente (com autorização)

```bash
# 1. Descobrir subdomínios
site:*.target.com

# 2. Encontrar tecnologias utilizadas
site:target.com intext:"powered by"
site:target.com intext:"running on"

# 3. Localizar interfaces administrativas
site:target.com (inurl:admin | inurl:manage | inurl:control)

# 4. Buscar endpoints de API
site:target.com (inurl:api | inurl:rest | inurl:graphql)

# 5. Verificar informações em cache
cache:target.com
```

### 🎯 Exemplo 3: Bug Bounty Research

**Objetivo**: Encontrar vulnerabilidades em programa autorizado

```bash
# 1. Buscar por diretórios listáveis
site:target.com intitle:"index of"

# 2. Procurar por arquivos de desenvolvimento
site:target.com (ext:dev | ext:test | ext:staging)

# 3. Localizar informações de debug
site:target.com (intext:debug | intext:error | intext:exception)

# 4. Buscar configurações de desenvolvimento
site:target.com (inurl:dev | inurl:test | inurl:debug)
```

---

## Proteção e Mitigação

### 🛡️ Para Administradores

**1. Auditoria Proativa:**
```bash
# Execute contra seus próprios domínios
site:seudominio.com (ext:conf | ext:env | ext:bak)
site:seudominio.com intitle:"index of"
site:seudominio.com inurl:admin
```

**2. Configuração do robots.txt:**
```
User-agent: *
Disallow: /admin/
Disallow: /config/
Disallow: /backup/
Disallow: /*.conf$
Disallow: /*.env$
Disallow: /*.bak$
```

**3. Configuração do servidor web:**
```apache
# Apache - Bloquear arquivos sensíveis
<FilesMatch "\.(conf|config|env|bak|backup|old|log)$">
    Order allow,deny
    Deny from all
</FilesMatch>
```

```nginx
# Nginx - Bloquear arquivos sensíveis
location ~* \.(conf|config|env|bak|backup|old|log)$ {
    deny all;
    return 404;
}
```

**4. Revisão de Permissões:**
- Remover indexação de diretórios desnecessários
- Configurar autenticação em painéis admin
- Criptografar dados sensíveis
- Implementar rate limiting para buscas

### 🔒 Remoção de Resultados

**Google Search Console:**
1. Acesse o Google Search Console
2. Vá em "Remoções" → "Nova solicitação"
3. Insira a URL a ser removida
4. Aguarde processamento (pode levar semanas)

**Métodos complementares:**
- Configure cabeçalhos `noindex, nofollow`
- Use meta tags `<meta name="robots" content="noindex">`
- Implemente autenticação HTTP Basic
- Remova fisicamente arquivos sensíveis

---

## OPSEC para Investigadores

### 🔍 Boas Práticas de Investigação

**1. Anonimização:**
- Use VPN confiável
- Navegue através de Tor quando apropriado
- Utilize máquinas virtuais isoladas
- Evite login em contas pessoais

**2. Documentação Segura:**
- Não inclua URLs completas em relatórios
- Censure informações sensíveis em capturas
- Use nomes de arquivo neutros (`target_finding_01.png`)
- Mantenha evidências em ambiente isolado

**3. Escalação Responsável:**
```markdown
# Template de Disclosure Responsável

Assunto: [CONFIDENCIAL] Descoberta de Segurança - [DOMINIO]

Prezados,

Durante uma auditoria de segurança autorizada, identificamos a seguinte exposição:

- **Tipo**: [Descrição da vulnerabilidade]
- **Impacto**: [Baixo/Médio/Alto/Crítico]
- **Localização**: [URL censurada]
- **Evidência**: [Anexo com dados sensíveis removidos]

Recomendações:
1. [Ação imediata necessária]
2. [Configuração preventiva]

Atenciosamente,
[Seu nome/empresa]
```

**4. Limites Legais:**
- Sempre obtenha autorização por escrito
- Respeite escopos definidos em contratos
- Não acesse sistemas sem permissão
- Pare imediatamente se encontrar dados pessoais

### ⚠️ Sinais de Alerta

**Pare a investigação se encontrar:**
- Dados pessoais (CPF, passaportes, etc.)
- Informações médicas
- Dados financeiros de terceiros
- Conteúdo protegido por direitos autorais
- Sistemas governamentais/militares

---

## Dorks Prontos por Categoria

### 🚀 Quick Start - Dorks Essenciais

```bash
# Configurações expostas
site:"[DOMINIO]" (ext:conf | ext:config | ext:env | ext:ini | ext:cnf)

# Backups esquecidos
site:"[DOMINIO]" (inurl:backup | ext:bak | ext:backup | ext:old | ext:swp)

# Documentos sensíveis
site:"[DOMINIO]" (ext:pdf | ext:doc | ext:docx | ext:xls | ext:xlsx) (intext:"confidencial" | intext:"confidential")

# Painéis administrativos
site:"[DOMINIO]" (inurl:admin | inurl:administrator | intitle:"admin" | intitle:"login")

# APIs expostas
site:"[DOMINIO]" (inurl:api | inurl:rest | inurl:graphql | inurl:v1 | inurl:v2)

# Logs com informações sensíveis
site:"[DOMINIO]" (ext:log | inurl:log) (intext:password | intext:error | intext:exception)

# Indexação de diretórios
site:"[DOMINIO]" intitle:"index of" (intext:"parent directory" | intext:"last modified")
```

### 🎯 Dorks Específicos por Tecnologia

**WordPress:**
```bash
site:"[DOMINIO]" inurl:wp-config.php intext:DB_PASSWORD
site:"[DOMINIO]" inurl:wp-content/uploads/ filetype:sql
site:"[DOMINIO]" intitle:"Index of" wp-admin
```

**AWS/Cloud:**
```bash
site:"[DOMINIO]" (intext:aws_access_key_id | intext:aws_secret_access_key)
site:s3.amazonaws.com "[EMPRESA]"
intext:"ARTIFACTS_AWS_ACCESS_KEY_ID"
```

**Git Repositories:**
```bash
site:"[DOMINIO]" inurl:.git
site:"[DOMINIO]" intext:"index of" intext:".git"
site:github.com "[EMPRESA]" intext:password
```

---

## ⚖️ Aspectos Legais e Éticos

### ✅ Uso Autorizado
- Auditoria de segurança em domínios próprios
- Pentesting com contrato assinado
- Bug bounty em programas públicos
- Pesquisa acadêmica com aprovação ética
- Treinamento em ambientes controlados

### ❌ Uso Proibido
- Acesso não autorizado a sistemas
- Coleta de dados pessoais sem consentimento
- Bypass de controles de acesso
- Download de material protegido
- Uso para fins maliciosos

### 📋 Checklist Legal
- [ ] Autorização por escrito obtida
- [ ] Escopo claramente definido
- [ ] Compliance com leis locais
- [ ] Processo de disclosure definido
- [ ] Seguro de responsabilidade ativo

---

## 🔗 Recursos Adicionais

**Ferramentas Complementares:**
- **Shodan**: Para descoberta de serviços expostos
- **Censys**: Mapeamento de certificados e serviços
- **TheHarvester**: Coleta automatizada de informações
- **recon-ng**: Framework de reconhecimento
- **FOCA**: Extração de metadados de documentos

**Bases de Conhecimento:**
- OWASP Testing Guide
- NIST Cybersecurity Framework
- SANS OSINT Framework
- Exploit Database (exploit-db.com)

**Monitoramento Contínuo:**
- Configure alertas para menções da empresa
- Monitore vazamentos em pastebin/github
- Automatize varreduras periódicas
- Mantenha inventário de assets externos

---

## 📝 Considerações Finais

Google Dorks são ferramentas poderosas que devem ser usadas com responsabilidade. Para investigadores OSINT:

1. **Sempre obtenha autorização antes de investigar**
2. **Respeite limites legais e éticos**
3. **Documente achados de forma segura**
4. **Relate vulnerabilidades responsavelmente**
5. **Mantenha-se atualizado com leis locais**

Lembre-se: o objetivo do OSINT defensivo é **proteger**, não atacar. Use esses conhecimentos para fortalecer a segurança, educar equipes e melhorar a postura de segurança organizacional.

---

> **Disclaimer**: As informações neste guia são apenas para fins educacionais e de segurança defensiva. O uso inadequado dessas técnicas pode violar leis locais e termos de serviço. O autor não se responsabiliza por uso indevido do conteúdo apresentado.