# Infraestrutura de Domínios e IPs

## Objetivo
Mapear ativos digitais (domínios, IPs, ASN e certificados) para revelar relações entre sistemas, proprietários e superfícies de ataque.

## Preparação Rápida
1. Reúna domínio, IP ou ASN inicial e defina escopo temporal.
2. Organize uma planilha de pivô (domínio → IP → serviço) usando o modelo de dossiê.
3. Garanta isolamento operacional antes de consultar serviços sensíveis.

## Registros e Whois
- [Whois](https://who.is) — consulta rápida de registrante e datas-chave.
- [ICANN Lookup](https://lookup.icann.org/) — dados oficiais de registro global.
- [ARIN](https://www.arin.net/) / [RIPE](https://www.ripe.net/) / [LACNIC](https://www.lacnic.net/) / [APNIC](https://www.apnic.net/) / [AFRINIC](https://www.afrinic.net/) — registros regionais de IP.
- [APNIC WhoWas](https://www.apnic.net/static/whowas-ui/) — histórico de delegações na Ásia-Pacífico.

## Inteligência de Domínios
- [SecurityTrails](https://securitytrails.com/) — visão consolidada de DNS, subdomínios e históricos.
- [DomainTools](https://domaintools.com) — pivôs por registrante, servidor DNS e histórico WHOIS.
- [Robtex](https://robtex.com/) — grafo de relações entre IPs, domínios e serviços.
- [DomainBigData](https://domainbigdata.com/) — vínculos por e-mail de cadastro e NS.

## Certificados e DNS Passivo
- [crt.sh](https://crt.sh/) — logs de Certificate Transparency para novos subdomínios.
- [CertDB](https://certdb.com) — catálogo histórico de certificados SSL/TLS.
- [PassiveDNS Mnemonic](https://passivedns.mnemonic.no/) — resoluções históricas para pivotar IP ↔ domínio.
- [DNSDumpster](https://dnsdumpster.com/) — mapa de registros DNS e infraestrutura exposta.

## Fingerprinting e Tecnologias
- [BuiltWith](https://builtwith.com/) — identifica stacks tecnológicos e tags analíticas.
- [Wappalyzer](https://www.wappalyzer.com/) — detecta CMS, frameworks e bibliotecas.
- [Netcraft Site Report](https://toolbar.netcraft.com/site_report?url=) — servidores, certificados e hosting.
- [SpyOnWeb](https://spyonweb.com/) — cruza IDs de analytics e AdSense.

## Utilitários de IP
- [IPVoid](https://www.ipvoid.com/) — reputação e blacklist.
- [CentralOps](https://centralops.net/) — suíte de consultas WHOIS, traceroute, ping.
- [GeoIP Tool](https://geoiptool.com/) — geolocalização aproximada de IP.
- [I Know What You Download](https://iknowwhatyoudownload.com/en/peer/) — histórico de torrents associado a IP público.

## Histórico de Domínios
- [CarbonDate](https://carbondate.cs.odu.edu/) — estimativa de primeira aparição pública.
- [CompleteDNS](https://completedns.com/dns-history/) — timeline de registros DNS.
- [WhoisRequest](https://whoisrequest.com/history/) — histórico de propriedades.
- [Timer4Web](http://timer4web.com) — monitoramento de mudanças com alertas.

## Boas Práticas
- Utilize CT logs e passive DNS antes de rodar scans ativos.
- Consolide pivôs em gráfico (domínio → subdomínio → IP → ASN) para identificar clusters.
- Registre cada consulta com data e confiança no dossiê investigativo.

## Alertas de OPSEC
- Evite buscas autenticadas com identidade real.
- Respeite limites de requisições para não bloquear ferramentas críticas.
- Para investigações sensíveis, prefira VPN + máquinas isoladas.
