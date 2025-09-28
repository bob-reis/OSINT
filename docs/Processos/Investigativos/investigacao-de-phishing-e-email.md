# Investigação de Phishing e E-mails

## Objetivo
Avaliar reputação de endereços, validar cabeçalhos e identificar kits de phishing reutilizados para mitigar campanhas maliciosas.

## Preparação Rápida
1. Colete mensagem completa (incluindo cabeçalhos e anexos) em ambiente isolado.
2. Identifique indicadores iniciais: remetente, URLs, IPs, hashes.
3. Defina plano de validação cruzando com feeds e bases de vazamentos.

## Reputação e Vazamentos
- [Have I Been Pwned](https://haveibeenpwned.com/) — verifica exposição em vazamentos públicos.
- [DeHashed](https://dehashed.com/) — busca credenciais e registros correlatos (uso controlado).
- [EmailRep.io](https://emailrep.io/) — reputação com classificação de risco.
- [Hunter.io](https://hunter.io/) — padrões de e-mail corporativo para confirmar spoofing.

## Análise Técnica de E-mail
- [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx) — interpreta Received, SPF, DKIM.
- [Mailtester](http://mailtester.com/) — checa existência de mailbox sem envio.
- [VerifyEmailAddress.io](https://tools.verifyemailaddress.io/) — confirma entregabilidade.

## Verificação de URLs Suspeitas
- [urlscan.io](https://urlscan.io/) — sandbox visual de URLs e recursos carregados.
- [URLQuery](http://urlquery.net) — análise comportamental com indicadores IOC.
- [PhishTank](https://phishtank.org/) — base colaborativa para checar/dominar phishing.
- [OpenPhish](https://openphish.com/) — feed automatizado de URLs maliciosas.
- [StalkPhish](https://github.com/t4d/StalkPhish) — identifica kits reutilizados e hosting compartilhado.

## Enriquecimento de IOC
- [Maltiverse](https://maltiverse.com/search) — consolida domínio/IP/hash com reputação.
- [ThreatCrowd](https://threatcrowd.org/) — grafo relacionando e-mails, domínios e IPs.
- [ThreatMiner](https://www.threatminer.org/) — metadados de malware e indicadores relacionados.

## Boas Práticas
- Abra e-mails suspeitos apenas em máquinas de análise (isoladas ou VMs).
- Gere hashes dos anexos antes de enviar para sandbox externa.
- Documente cadeia de evidências em `docs/modelos/dossie-investigativo.md`.

## Alertas de OPSEC
- Nunca interaja com links de phishing a partir de redes produtivas.
- Evite autenticar-se em serviços de reputação com contas pessoais.
- Verifique legislação local antes de coletar dados de terceiros comprometidos.
