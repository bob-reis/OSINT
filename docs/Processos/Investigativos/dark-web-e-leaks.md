# Dark Web e Vazamentos

## Objetivo
Localizar serviços Onion relevantes, monitorar vazamentos e correlacionar dados obtidos com indicadores investigativos, sempre respeitando limites legais.

## Preparação Rápida
1. Configure ambiente isolado (VM + Tor) e persona dedicada.
2. Defina palavras-chave e alvos (marketplaces, fóruns, dumps).
3. Planeje coleta segura: snapshots, hashes, anonimização.

## Buscadores Onion
- [Ahmia](https://ahmia.fi) — indexa hidden services com filtros por categoria.
- [Haystak](http://haystak5njsmn2hqkewecpaxetahtwhsbsa64jom2k22z5afxhnpxfid.onion/) — pesquisa full-text (versão paga amplia resultados).
- [Torch](http://torchdeedp3i2jigzjdmfpn5ttjhthh5wbmda2rr3jvqjg5p77c54dqd.onion/) — veterano com alto volume de páginas.
- [Kilos](http://mlyusr6htlxsyc7t2f4z53wdxh3win7q3qpxcrbam6jf3dmua7tnzuyd.onion/captcha) — referência para mercados e fóruns.
- [Tor66](http://tor66sewebgixwhcqfnp5inzp5x5uohhdy3kvtnyfxc2e5mxiuh34iid.onion/) — catálogo com mirror de serviços ativos.

## Diretórios e Monitoramento
- [Dark.fail](http://darkfailenbsdla5mal2mxn2uz66od5vtzd5qozslagrfzachha3f3id.onion/) — monitora uptime e chaves PGP.
- [Onion.Live](https://onion.live/) — status de serviços, reputação e categorias.
- [The Hidden Wiki](http://paavlaytlfsqyvkg3yqj7hflfg5jw2jdg2fgkza5ruf6lplwseeqtvyd.onion/) — diretório comunitário (validar links).
- [Tor.Taxi](http://tortaxi7axhn2fv4j475a6blv7vwjtpieokolfnojwvkhsnj7sgctkqd.onion/) — portal seguro com curadoria.

## Vazamentos e Dumps
- [Breached.to](https://breached.to/) — fórum focado em dumps e vendas (alto risco).
- [IntelligenceX](https://intelx.io) — indexa dumps, documentos e Onion (acesso com conta).
- [OCCRP Aleph](https://data.occrp.org) — vazamentos públicos verificados.
- [DarkSearch](https://darksearch.io) — busca via clearnet em índices Onion.

## Ferramentas de Apoio
- [IACA Dark Web Tools](https://iaca-darkweb-tools.com) — utilitários para investigadores (hashing, conversões).
- [Google CSE Utopia](https://start.me/p/EL84Km/cse-utopia) — coleções de Custom Search Engines.
- [Napalm FTP Indexer](https://www.searchftps.net) — FTPs expostos com dumps históricos.
- [Archive.org](https://archive.org) — espelha dumps públicos e postagens antigas.

## Boas Práticas
- Valide URLs e chaves PGP oficiais antes de autenticar.
- Baixe conteúdo suspeito em sandboxes isoladas e gere hashes imediatamente.
- Registre fonte Onion, data e nível de confiança no dossiê.

## Alertas de OPSEC
- Nunca acesse marketplaces com identidade real ou IP corporativo.
- Atenção a conteúdo ilegal — interrompa coleta e reporte conforme leis locais.
- Utilize personas com `docs/Processos/criacao-de-fantoche-sock-puppet.md` para interações.
