# Arquivamento e Cache Web

## Objetivo
Preservar evidências online voláteis (páginas, vídeos, posts) garantindo integridade e possibilidade de auditoria futura.

## Preparação Rápida
1. Capture contexto inicial: URL, data/hora, capturas de tela.
2. Escolha arquivadores redundantes (Wayback + Archive.today, por exemplo).
3. Armazene hashes e notas no dossiê investigativo.

## Arquivos Web Principais
- [Wayback Machine](https://archive.org/web/) — maior acervo histórico de páginas.
- [Archive.today](https://archive.today/) — snapshot sob demanda, contorna paywalls simples.
- [Memento Time Travel](http://timetravel.mementoweb.org/) — agrega múltiplos provedores de arquivo.
- [Perma.cc](https://perma.cc/) — preservação voltada a citações acadêmicas/jurídicas.
- [Ghostarchive](https://ghostarchive.org/) — foca em vídeos e postagens de redes sociais.

## Páginas em Cache
- [CachedView](http://cachedview.com/) — visualiza cópias do Google e Wayback.
- `cache:exemplo.com` (Google) — acessa versões recentes via buscador.
- `https://cc.bingj.com/cache.aspx` — obtém cache do Bing quando disponível.
- [CoralCDN](http://www.coralcdn.org/) — espelho colaborativo para sites populares.

## Arquivamento de Mídia Social e Vídeo
- [Save Page Now](https://web.archive.org/save) — força captura imediata na Wayback.
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — download de vídeos com metadados.
- [ArchiveBox](https://github.com/ArchiveBox/ArchiveBox) — solução self-hosted para coleções grandes.
- [SingleFile](https://github.com/gildas-lormeau/SingleFile) — extensão para salvar página como HTML único.

## Boas Práticas
- Execute duas capturas redundantes (Wayback + arquivo local) para robustez.
- Salve cabeçalhos HTTP e resposta bruta quando houver suspeita de alteração futura.
- Vincule cada evidência à fonte com timestamp e confiança no dossiê.

## Alertas de OPSEC
- Alguns serviços registram IP; use VPN/persona quando necessário.
- Respeite leis de direitos autorais ao redistribuir conteúdo arquivado.
- Evite arquivar materiais ilegais; reporte conforme políticas regionais.
