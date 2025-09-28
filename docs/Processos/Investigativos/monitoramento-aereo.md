# Monitoramento de Aeronaves

## Objetivo
Realizar rastreamento de aeronaves civis e militares, correlacionando rotas, proprietários e históricos de voo relevantes para investigações OSINT.

## Preparação Rápida
1. Identifique ICAO, prefixo ou rota de interesse.
2. Defina período de análise (tempo real vs. histórico).
3. Planeje como registrar capturas e exportar dados sem violar termos de uso.

## Rastreamento em Tempo Real
- [ADS-B Exchange](https://www.adsbexchange.com/) — radar colaborativo sem filtros comerciais.
- [RadarBox](https://www.radarbox24.com/) — visualização global com dados de altitude/velocidade.
- [Flightradar24](https://www.flightradar24.com/) — cobertura mundial com camadas de meteo.
- [FlightAware](https://flightaware.com) — dashboards e alertas customizados.
- [LiveATC](https://www.liveatc.net/) — áudio de torres para confirmar operações.

## Dados Históricos
- [ADS-B Exchange Flight Data](https://flight-data.adsbexchange.com) — registros CSV e KMZ para análise offline.
- [OpenSky Network](https://opensky-network.org/network/explorer) — histórico com API pública.
- [Planespotters](https://www.planespotters.net/) — registro de aeronaves, operadores e fotos.
- [Casper Flights](http://casperflights.com) — revisualização de rotas anteriores.

## Bases de Aeronaves e Propriedade
- [OpenSky Aircraft DB](https://opensky-network.org/aircraft-database/) — metadados de aeronaves registradas.
- [JetPhotos](https://www.jetphotos.com/) — confirma livery e alterações visuais.
- [Airframes](http://www.airframes.org) — histórico de proprietários e status.
- [FlightConnections](https://www.flightconnections.com) — mapa de rotas comerciais por companhia.

## Complementos Militares e Governamentais
- [GVA Dictator Alert](https://github.com/lefranz/geneva-dictators) — monitoramento de aeronaves governamentais.
- [Planeflighttracker](http://www.planeflighttracker.com/2014/04/united-states-military-aircraft-in.html) — listagens de aeronaves militares dos EUA.
- [Live Military Mode-S](https://www.live-military-mode-s.eu/) — captura de sinais militares europeus.

## Boas Práticas
- Combine registros ADS-B com áudio ATC para confirmar pousos e decolagens.
- Utilize camadas meteorológicas para explicar desvios de rota.
- Documente cada captura em `docs/modelos/dossie-investigativo.md` com fonte, data e confiança.

## Alertas de OPSEC
- Evite logins pessoais em plataformas que exigem cadastro.
- Atenção a políticas locais sobre redistribuição de dados ADS-B.
- Considere uso de máquinas virtuais quando executar scripts de coleta automatizada.
