# Análise de Vídeo

## Objetivo
Validar autenticidade, origem e contexto de vídeos, extraindo metadados e correlacionando com outras evidências multimídia.

## Preparação Rápida
1. Baixe cópia do vídeo mantendo o arquivo original intacto.
2. Gere hash e registre dados iniciais (fonte, data, canal) no dossiê.
3. Defina hipóteses (ex.: manipulação, localização, linha do tempo).

## Verificação e Metadados
- [InVID/WeVerify](https://www.invid-project.eu/tools-and-services/invid-verification-plugin/) — plugin com keyframes, análise forense e pesquisa reversa.
- [YouTube DataViewer](https://citizenevidence.amnestyusa.org/) — extrai ID, upload e miniaturas para busca.
- [Amnesty YouTube Metadata](https://citizenevidence.amnestyusa.org/) — verificação rápida e arquivamento.

## Download e Preservação
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — CLI robusta para download com metadados.
- [4K Video Downloader](https://www.4kdownload.com/products/product-videodownloader) — alternativa GUI multiplataforma.
- [SaveFrom](https://en.savefrom.net/) — solução rápida (usar com segurança operacional).

## Monitoramento de Transmissões
- [TwitchTracker](https://twitchtracker.com/) — histórico de streamers e estatísticas.
- [Streamscharts](https://streamscharts.com/) — análise comparativa de audiências ao vivo.
- [CrowdTangle](https://www.crowdtangle.com/) — monitoramento de vídeos em redes Meta (acesso restrito).

## Detecção de Manipulações
- [Deepware Scanner](https://deepware.ai/) — identifica deepfakes em arquivos locais.
- [Sensity AI](https://sensity.ai/) — solução corporativa para ameaças visuais.
- [Microsoft Video Authenticator](https://news.microsoft.com/on-the-issues/2020/09/01/microsoft-disinformation-deepfakes-new-technology/) — validação de frame (acesso sob demanda).

## Boas Práticas
- Capture frames-chave e compare com busca de imagem para geolocalização.
- Sincronize metadados com eventos conhecidos (notícias, registros públicos).
- Utilize `docs/modelos/dossie-investigativo.md` para consolidar achados.

## Alertas de OPSEC
- Execute downloads a partir de identidades isoladas para evitar marcações.
- Tenha cautela com plugins de navegador em ambientes sensíveis.
- Preserve cadeia de custódia para eventual uso jurídico.
