# LinkedIn — Investigações OSINT

## Visão Geral
LinkedIn reúne mais de 1,2 bilhão de perfis e foi desenhado para uso profissional. Movimentações de carreira, conexões e conteúdos formam um banco de dados voluntário que pode revelar intenções estratégicas, parcerias e lacunas de segurança. Essa investigação deve observar limites legais, termos de uso e diretrizes de OPSEC descritas em `CLAUDE.md`.

## Sinais Principais
- Movimentação de funcionários indica aquisições, mudanças de equipe e novos projetos.
- Vagas abertas expõem prioridades, tecnologias adotadas e expansão geográfica.
- Padrões de conexão evidenciam redes de influência, fornecedores e parceiros.
- Postagens e artigos mostram narrativas estratégicas e posicionamento executivo.

## Casos de Uso Prioritários
- **Investigação corporativa:** mapear organograma, tomadores de decisão e conflitos de interesse.
- **Atribuição de ameaças:** correlacionar competências técnicas com incidentes reportados.
- **Due diligence e compliance:** validar histórico profissional, vínculos societários e riscos regulatórios.
- **Inteligência competitiva:** acompanhar contratações críticas, anúncios de produtos e presença em eventos.
- **Detecção de insider/fraude:** observar conexões atípicas com concorrentes e mudanças abruptas de comportamento.

## Preparação e OPSEC
- Ative o modo privado (`Configurações > Visibilidade > Modo privado`) antes de visitar perfis.
- Utilize sock puppets documentados nos checklists de OPSEC para evitar exposição do investigador.
- Registre data, hora, palavras-chave e filtros aplicados para rastreabilidade.

## Técnicas de Coleta
- Explore filtros nativos (Posts, Pessoas, Vagas, Grupos, Empresas, Eventos) e o botão **All filters** para combinar critérios.
- Aplique operadores booleanos (`"open source intelligence"`, `(analyst OR researcher) AND (OSINT OR "open source")`) para refinar buscas.
- Utilize Google dorks para exceder limites da busca interna: `site:linkedin.com "Chief Information Security Officer" "São Paulo"`.
- Apoie-se em buscadores dedicados (LinkedIn Contact Extractor, DorkGPT, RecruitEm) para automatizar consultas e scraping autorizado.

## Análise de Perfis
- **Imagens e banner:** execute busca reversa (Google, Yandex, PimEyes) para localizar contas espelhadas ou material compromissor.
- **Informações de contato:** e-mails, telefones e URLs devem ser cruzados com vazamentos, WHOIS e Wayback Machine; atenção a PII.
- **Nome de usuário x exibição:** compare `linkedin.com/in/username` com usos em outras redes via Usersearch ou Namevine.
- **Sobre, Experiência e Educação:** reconstruir linha do tempo, validar certificações, identificar lacunas e projetos nomeados (ex.: "Project Delta").
- **Skills e Recomendações:** priorize competências com endossos consistentes e relatos de terceiros que mencionem entregas, equipes ou ferramentas específicas.

## Postagens, Comentários e Metadados
- Classifique o tom do texto e extraia hashtags para novas pivotações.
- Analise imagens e vídeos em busca de logotipos, telas, IPs ou ambientes reconhecíveis; amplie se necessário.
- Capture timestamps, geotags e cadeias de comentários para entender contexto, alcance e reações do público.
- Observe como o alvo interage (respostas rápidas, complementos de informação, defensividade) para avaliar abertura e narrativa.

## Páginas Corporativas
- Verifique consistência entre nome da página e domínio oficial; procure variações suspeitas.
- Faça busca reversa em logotipo e banner para confirmar autenticidade e identificar eventos associados.
- Utilize seções **About**, **People** e **Jobs** para cruzar headcount, cargos críticos e iniciativas recentes.
- Acompanhe frequência de publicações e engajamento para medir atividade e maturidade digital.

## Limitações Frequentes
1. **Dados auto declarados:** títulos e datas podem ser inflados; valide com comunicados oficiais e bases independentes.
2. **Lacunas temporais:** intervalos não explicados exigem investigação complementar.
3. **Endossos inflados:** popularidade não garante domínio técnico.
4. **Configurações de privacidade:** visibilidade varia conforme grau de conexão e tipo de assinatura.
5. **Perfis falsos:** compare fotos, cronologia e terminologia com outras fontes antes de confiar.

## Preservação de Evidências
- Capture páginas completas com ferramentas de arquivamento certificadas (ex.: WebPreserver) para manter metadados e cadeia de custódia.
- Faça screenshots somente como apoio visual, garantindo armazenamento seguro e hash da imagem.
- Registre fluxo de coleta (data, hora, filtros, URLs) em `docs/modelos/dossie-investigativo.md` para reprodutibilidade.

## Referências Úteis
- LinkedIn — [news.linkedin.com/about-us](https://news.linkedin.com/about-us)
- Ferramentas de dorking: DorkGPT, Dorksearch, RecruitEm, Google Dork Generator
- Buscas reversas: Google Imagens, TinEye, Yandex, Bing Visual, PimEyes
- Análise de metadados: ExifTool, EXIF.tools, Azure AI Vision
