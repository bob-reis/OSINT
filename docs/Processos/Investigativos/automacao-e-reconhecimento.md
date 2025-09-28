# Automação e Frameworks de Reconhecimento

## Objetivo
Acelerar coletas repetitivas e enriquecimento de dados utilizando frameworks modulares, mantendo rastreabilidade das fontes.

## Preparação Rápida
1. Defina escopo (domínio, pessoa, infraestrutura) e limites de consulta.
2. Configure ambiente isolado (VM, contêiner) para evitar vazamento de credenciais.
3. Planeje registro automatizado de evidências no modelo de dossiê.

## Frameworks Principais
- [SpiderFoot](https://www.spiderfoot.net/) — mais de 200 módulos para pivotar em domínios, e-mails e IPs.
- [Recon-ng](https://github.com/lanmaster53/recon-ng) — workspace CLI com integrações de API.
- [Maltego](https://www.maltego.com/) — análise gráfica com transformações avançadas.
- [OSRFramework](https://github.com/i3visio/osrframework) — foco em enumeração de identidades digitais.
- [theHarvester](https://github.com/laramies/theHarvester) — coleta emails/hosts/subdomínios a partir de buscadores.
- [datasploit](https://github.com/DataSploit/datasploit) — automações para pivotar informações de alvos.

## Extensões e Utilitários
- [Mitaka](https://github.com/ninoseki/mitaka) — investiga IOC diretamente na barra do navegador.
- [Shodan Plugin](https://chrome.google.com/webstore/detail/shodan/jjalcfnidlmpjhdfepjhjbhnhkbgleap) — consulta ativos expostos sem sair da página.
- [Wappalyzer](https://www.wappalyzer.com/apps) — identifica tecnologias web instantaneamente.

## Metadados e Documentos
- [Metagoofil](https://www.edge-security.com/metagoofil.php) — extrai metadados de documentos públicos.
- [FOCA](https://github.com/ElevenPaths/FOCA) — analisa documentos para revelar servidores internos e usuários.
- [bulk_extractor](https://github.com/simsong/bulk_extractor) — extrai artefatos digitais em massa.

## Plataformas Auto-Hospedadas
- [Cortex](https://github.com/TheHive-Project/Cortex) — orquestra análises de observáveis via API.
- [IntelOwl](https://github.com/intelowlproject/IntelOwl) — centraliza consultas em OSINT/Threat Intel.
- [OpenCTI](https://www.opencti.io/en/) — gerencia conhecimento de ameaças com relacionamentos.
- [Kali Linux](https://www.kali.org/) — distribuição com arsenal de coleta/automação.

## Boas Práticas
- Armazene chaves de API em cofres seguros; não versione segredos.
- Controle uso de módulos agressivos para evitar detecção.
- Revise logs de execução e exporte resultados relevantes para o dossiê.

## Alertas de OPSEC
- Utilize contas descartáveis para integrações de terceiros.
- Monitore limites de API para evitar bloqueios e exposição da investigação.
- Atualize frameworks regularmente para corrigir módulos obsoletos.
