# Feeds de Inteligência

## Objetivo
Consumir indicadores atualizados de ameaças (IOC) para enriquecer investigações, correlacionar incidentes e antecipar riscos.

## Preparação Rápida
1. Defina escopo (URL, IP, hash, certificado) e formato necessário (CSV, API, RSS).
2. Configure automações para importar feeds de forma segura (scripts isolados).
3. Documente origem, data e confiança de cada indicador ingestido.

## Feeds Comunitários
- [ThreatFox](https://threatfox.abuse.ch/) — IOCs submetidos pela comunidade.
- [URLhaus](https://urlhaus.abuse.ch/) — URLs maliciosas ativas.
- [Feodo Tracker](https://feodotracker.abuse.ch/) — C2s de trojans bancários.
- [MalwareBazaar](https://bazaar.abuse.ch/) — amostras de malware e hashes.
- [AlienVault OTX](https://otx.alienvault.com/) — pulse sharing colaborativo.

## Feeds Especializados/Comerciais
- [Spamhaus](https://www.spamhaus.org/) — listas reputacionais de IPs/domínios.
- [AbuseIPDB](https://www.abuseipdb.com/) — IPs denunciados por abuso.
- [CIRCL OSINT Feeds](https://www.circl.lu/services/osint/) — coletas do CERT luxemburguês.
- [Abuse.ch SSLBL](https://sslbl.abuse.ch/) — certificados SSL suspeitos.
- [OpenPhish](https://openphish.com/) — feed automatizado de phishing.
- [PhishTank](https://phishtank.org/) — repositório colaborativo (exportável).

## Exposição e Superfície de Ataque
- [GreyNoise](https://www.greynoise.io/) — contexto para tráfego de scanners.
- [Shodan Alerts](https://www.shodan.io/alerts) — monitora ativos expostos.
- [Censys](https://censys.io/) — inventário global com atributos detalhados.

## Boas Práticas
- Normalize indicadores (IOC) antes de inserir em SIEM/TI.
- Crie processo de expiração para evitar uso de dados obsoletos.
- Atribua confiança e notas de validação no dossiê investigativo.

## Alertas de OPSEC
- Utilize chaves de API segregadas para cada projeto.
- Respeite termos de uso ao redistribuir feeds comerciais.
- Configure limites de requisições para evitar bloqueios.
