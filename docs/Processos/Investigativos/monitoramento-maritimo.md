# Monitoramento Marítimo

## Objetivo
Rastrear embarcações comerciais, militares e de pesca, identificando proprietários, rotas e eventos relevantes para investigações marítimas.

## Preparação Rápida
1. Identifique MMSI, IMO ou nome da embarcação alvo.
2. Determine região e janela temporal de interesse.
3. Garanta registro de evidências em `assets/` com nomes neutros.

## Dados de Propriedade e Identificação
- [Equasis](http://www.equasis.org/EquasisWeb/public/HomePage) — cadastro global de navios e operadores.
- [Maritime Database](https://www.maritime-database.com) — histórico de armadores e bandeiras.
- [SuperYachts.com](https://www.superyachts.com) — foco em embarcações de luxo e rotas.

## Rastreamento AIS em Tempo Real
- [MarineTraffic](https://www.marinetraffic.com) — mapa global AIS com alertas customizáveis.
- [VesselFinder](https://www.vesselfinder.com) — posições em tempo real com detalhes técnicos.
- [VesselTracker](https://www.vesseltracker.com) — complementa com dados portuários.
- [MyShipTracking](https://www.myshiptracking.com) — interface leve para consultas rápidas.
- [CruiseMapper](http://www.cruisemapper.com) — itinerários de cruzeiros.

## Ferramentas Regionais e Especializadas
- [Global Fishing Watch](https://globalfishingwatch.org/map) — monitoramento de pesca industrial.
- [HELCOM AIS Explorer](http://maps.helcom.fi/website/AISexplorer) — tráfego no Mar Báltico.
- [Marine Scotland AIS](http://marine.gov.scot/information/ais-shipping-trafficselected-ports) — dados da costa escocesa.
- [AIS Tracker Rússia](http://en.aistracker.ru/map7.asp) — painel regional com exportação.

## Rastreamento de Cargas e Containers
- [CargoTracking Utopiax](http://cargotracking.utopiax.org/containertracking.html) — hub para múltiplas companhias.
- [Container-Tracking.org](http://container-tracking.org) — consolida consultas por transportadora.
- [ShipmentLink](https://www.shipmentlink.com/servlet/TDB1_CargoTracking.do) — acompanhamento por número de conhecimento.

## Complementos de Inteligência
- [Naval Technology](https://www.naval-technology.com) — atualizações de frota e defesa.
- [Ports.com](http://ports.com) — fichas portuárias e calculadora de distância.
- [InfoMarine24](http://www.infomarine24.com) — notícias e incidentes marítimos.

## Boas Práticas
- Cruce dados AIS com imagens AIS/portos para validar operações suspeitas.
- Utilize camadas meteorológicas para explicar mudanças de rota.
- Documente fontes e confiança utilizando `docs/modelos/dossie-investigativo.md`.

## Alertas de OPSEC
- Evite criar contas pessoais em serviços que exigem cadastro — prefira personas.
- Respeite restrições locais sobre redistribuição de dados AIS.
- Automatize coletas com limites conservadores para não acionar bloqueios.
