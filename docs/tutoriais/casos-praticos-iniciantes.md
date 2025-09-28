# Casos Práticos para Iniciantes OSINT

## 🎯 Objetivo

Este guia apresenta 10 casos práticos progressivos para iniciantes aplicarem os conceitos aprendidos no [Tutorial OSINT](osint-para-iniciantes.md). Cada caso inclui contexto, objetivos, processo sugerido e gabarito de verificação.

---

## 📋 Antes de Começar

### Preparação Obrigatória
- ✅ Leu o [Tutorial OSINT para Iniciantes](osint-para-iniciantes.md)
- ✅ Configurou ambiente seguro (VPN, navegador dedicado)
- ✅ Criou sock puppet básico
- ✅ Tem template de documentação pronto

### Regras Éticas
- ⚠️ **Use apenas pessoas públicas** (políticos, jornalistas, influenciadores)
- ⚠️ **Respeite privacidade** e não colete dados pessoais sensíveis
- ⚠️ **Fins educacionais** apenas — não use para stalking ou assédio
- ⚠️ **Documente fontes** e mantenha ética profissional

---

## 🔰 Caso 1: Pessoa Pública Básica

### Contexto
Você precisa criar um perfil básico de um político local para verificar informações de campanha.

### Alvo Sugerido
Escolha um **prefeito** ou **vereador** da sua cidade.

### Objetivos
- [ ] Nome completo e apelidos conhecidos
- [ ] Idade aproximada e local de nascimento
- [ ] Formação acadêmica e profissional
- [ ] Partido político atual e histórico
- [ ] Presença em redes sociais (pelo menos 3 plataformas)

### Processo Sugerido
1. **Google básico**: `"Nome do Político" prefeito cidade`
2. **Site oficial**: Buscar biografia oficial
3. **Redes sociais**: Facebook, Instagram, Twitter
4. **Tribunal Eleitoral**: Declarações de campanha
5. **Jornais locais**: Matérias e entrevistas

### Tempo Estimado
2-3 horas

### Gabarito
- ✅ **5+ informações verificadas** com fontes diferentes
- ✅ **Documentação completa** com Valor/Fonte/Data/Confiança
- ✅ **Sem dados pessoais sensíveis** (CPF, endereço residencial, etc.)

---

## 🔰 Caso 2: Empresa Local

### Contexto
Você precisa fazer due diligence básica de uma empresa que está oferecendo serviços.

### Alvo Sugerido
Escolha uma **empresa de tecnologia** ou **consultoria** local.

### Objetivos
- [ ] Razão social e CNPJ
- [ ] Endereço e telefones de contato
- [ ] Sócios e proprietários principais
- [ ] Tempo de atividade e histórico
- [ ] Presença digital (site, redes sociais)

### Processo Sugerido
1. **CNPJ**: Receita Federal, Jucesp
2. **Google**: Nome da empresa + "reclamação" ou "review"
3. **LinkedIn**: Perfil corporativo e funcionários
4. **Reclame Aqui**: Reputação e reclamações
5. **Site oficial**: Análise técnica com Wappalyzer

### Tempo Estimado
2-3 horas

### Ferramentas Específicas
- Receita Federal (CNPJ)
- LinkedIn Sales Navigator (gratuito)
- Reclame Aqui
- Wappalyzer

---

## 🔰 Caso 3: Verificação de Notícia

### Contexto
Uma notícia viral nas redes sociais afirma que determinado evento aconteceu. Você precisa verificar.

### Alvo Sugerido
Escolha uma **notícia recente** (última semana) que viralizou no Twitter/X.

### Objetivos
- [ ] Primeira fonte da informação
- [ ] Fontes oficiais que confirmam ou negam
- [ ] Análise de imagens/vídeos (se houver)
- [ ] Timeline dos eventos
- [ ] Conclusão sobre veracidade

### Processo Sugerido
1. **Busca reversa**: TinEye nas imagens da notícia
2. **Google News**: Buscar cobertura de veículos confiáveis
3. **Redes sociais**: Rastrear primeira menção
4. **Fontes oficiais**: Sites governamentais, instituições
5. **Fact-checkers**: Aos Fatos, Comprova, Lupa

### Tempo Estimado
1-2 horas

---

## 🔰 Caso 4: Investigação de Username

### Contexto
Você encontrou um username suspeito em uma rede social e quer mapear sua presença digital.

### Alvo Sugerido
Escolha um **influenciador** ou **criador de conteúdo** com username único.

### Objetivos
- [ ] Presença em pelo menos 5 plataformas
- [ ] Informações de contato públicas
- [ ] Possíveis nomes reais associados
- [ ] Cronologia de atividade
- [ ] Padrões de comportamento

### Processo Sugerido
1. **Sherlock**: `sherlock usuario_alvo`
2. **Google**: `"usuario_alvo"` com aspas
3. **Busca manual**: Instagram, TikTok, YouTube
4. **WhatsMyName**: Verificação rápida
5. **Cross-reference**: Correlacionar informações

### Ferramentas Específicas
- Sherlock
- WhatsMyName
- Maigret (alternativa)

### Tempo Estimado
1-2 horas

---

## 🔰 Caso 5: Análise de Domínio

### Contexto
Você recebeu um link suspeito e precisa analisar o domínio antes de acessar.

### Alvo Sugerido
Escolha um **site de notícias** menos conhecido ou **blog** temático.

### Objetivos
- [ ] Informações WHOIS completas
- [ ] Tecnologias utilizadas
- [ ] Histórico no Wayback Machine
- [ ] Reputação e segurança
- [ ] Possíveis subdomínios

### Processo Sugerido
1. **WHOIS**: `whois exemplo.com`
2. **VirusTotal**: Análise de reputação
3. **Wayback Machine**: Histórico do site
4. **Wappalyzer**: Tecnologias e frameworks
5. **Sublist3r**: Enumeração de subdomínios

### Tempo Estimado
1-2 horas

---

## 🔰 Caso 6: Geolocalização Básica

### Contexto
Você tem uma foto de um evento público e precisa identificar o local exato.

### Alvo Sugerido
Escolha uma **foto de evento público** recente (festival, protesto, manifestação).

### Objetivos
- [ ] Cidade e região identificadas
- [ ] Rua ou local específico
- [ ] Pontos de referência (prédios, monumentos)
- [ ] Data/hora aproximada
- [ ] Contexto do evento

### Processo Sugerido
1. **Google Images**: Busca reversa da foto
2. **Yandex Images**: Alternativa mais eficaz para rostos
3. **Google Maps**: Street View da região
4. **Google Earth**: Vista aérea e histórico
5. **Redes sociais**: Hashtags e geotags do evento

### Tempo Estimado
2-3 horas

---

## 🔰 Caso 7: Investigação de Email

### Contexto
Você recebeu um email de um contato profissional e quer verificar sua legitimidade.

### Alvo Sugerido
Escolha um **email corporativo** de empresa real (ex: contato@empresa.com).

### Objetivos
- [ ] Validar existência do email
- [ ] Verificar domínio corporativo
- [ ] Histórico de vazamentos
- [ ] Redes sociais associadas
- [ ] Padrão de emails da empresa

### Processo Sugerido
1. **Hunter.io**: Validação e padrões de email
2. **Have I Been Pwned**: Histórico de vazamentos
3. **Holehe**: Verificação em plataformas
4. **WHOIS**: Análise do domínio
5. **Google**: `"email@domain.com"` -site:domain.com

### Tempo Estimado
1-2 horas

---

## 🔰 Caso 8: Análise de Perfil Falso

### Contexto
Suspeita de que um perfil em rede social pode ser falso/automatizado.

### Alvo Sugerido
Encontre um **perfil com poucos seguidores** mas atividade suspeita no Twitter/X.

### Objetivos
- [ ] Padrões de postagem (horários, frequência)
- [ ] Análise de fotos (busca reversa)
- [ ] Conexões e interações
- [ ] Consistência de informações
- [ ] Indicadores de automação

### Processo Sugerido
1. **TinEye**: Busca reversa da foto de perfil
2. **Bot Sentinel**: Análise de comportamento
3. **Social Blade**: Estatísticas de crescimento
4. **Análise manual**: Padrões de linguagem
5. **Cross-platform**: Verificar outras redes

### Tempo Estimado
2-3 horas

---

## 🔰 Caso 9: Investigação de Número de Telefone

### Contexto
Você recebeu uma ligação de número desconhecido e quer identificar.

### Alvo Sugerido
Use um **número público** de empresa ou organização.

### Objetivos
- [ ] Operadora e região
- [ ] Proprietário/empresa associada
- [ ] Histórico de reclamações
- [ ] Presença em diretórios
- [ ] Possíveis golpes reportados

### Processo Sugerido
1. **Google**: `"(11) 9999-9999"` com aspas
2. **Truecaller**: Identificação de chamadas
3. **Quem Perturba**: Base de reclamações
4. **WhatsApp**: Verificar se número existe
5. **Anatel**: Consulta de operadora

### Tempo Estimado
1 hora

---

## 🔰 Caso 10: Análise de Evento Social

### Contexto
Análise completa de um evento público recente usando múltiplas fontes.

### Alvo Sugerido
Escolha um **evento cultural** ou **conferência** recente na sua cidade.

### Objetivos
- [ ] Organizadores e patrocinadores
- [ ] Local e infraestrutura
- [ ] Participantes principais
- [ ] Cobertura midiática
- [ ] Impacto e repercussão

### Processo Sugerido
1. **Site oficial**: Informações básicas
2. **Redes sociais**: Hashtags e posts
3. **Notícias**: Cobertura jornalística
4. **LinkedIn**: Participantes e organizadores
5. **Instagram/Twitter**: Fotos e vídeos do evento

### Tempo Estimado
3-4 horas

---

## 📊 Sistema de Avaliação

### Para cada caso, avalie:

#### Completude (0-3 pontos)
- **3**: Todos objetivos alcançados
- **2**: Maioria dos objetivos (80%+)
- **1**: Objetivos parciais (50%+)
- **0**: Poucos objetivos (<50%)

#### Qualidade das Fontes (0-3 pontos)
- **3**: Múltiplas fontes independentes e confiáveis
- **2**: Algumas fontes confiáveis
- **1**: Fontes limitadas mas válidas
- **0**: Fontes questionáveis ou insuficientes

#### Documentação (0-3 pontos)
- **3**: Documentação completa e organizada
- **2**: Boa documentação com pequenas falhas
- **1**: Documentação básica
- **0**: Documentação insuficiente

#### OPSEC (0-1 ponto)
- **1**: Manteve segurança operacional
- **0**: Violou princípios de OPSEC

### Pontuação Total por Caso
- **9-10**: Excelente ⭐⭐⭐
- **7-8**: Bom ⭐⭐
- **5-6**: Satisfatório ⭐
- **<5**: Precisa melhorar

### Meta Global
**Objetivo**: Alcançar pelo menos **8 pontos** em 8 dos 10 casos.

---

## 🎯 Próximos Passos

### Após completar os casos:
1. **Auto-avaliação**: Use o sistema de pontuação
2. **Identifique padrões**: Quais tipos de investigação você domina?
3. **Áreas de melhoria**: Onde precisa praticar mais?
4. **Evolução**: Passe para a [Trilha Progressiva](trilha-progressiva-osint.md)

### Casos Avançados
Quando se sentir confortável, tente:
- Investigações multi-domínio
- Casos com prazo limitado
- Análise de grupos/organizações
- Threat intelligence básica

---

## 🤝 Compartilhamento e Comunidade

### Documente seu progresso:
- Crie um portfólio anonimizado
- Participe de grupos de estudo
- Mentore outros iniciantes
- Contribua com melhorias neste guia

**Lembre-se**: A prática leva à perfeição, mas a ética deve sempre vir primeiro!