# Pessoas e Redes Sociais

## Objetivo
Guiar investigações em perfis públicos a partir de identidades digitais, correlacionando contas, conteúdos e redes de relacionamento.

## Preparação Rápida
1. Defina hipótese investigativa (ex.: confirmar propriedade de um @username).
2. Reúna identificadores iniciais (apelidos, e-mails, números, fotos).
3. Estabeleça limites de coleta e requisitos de OPSEC conforme `checklists/checklist-opsec.md`.

## Ferramentas Multiplataforma
- [Sherlock](https://github.com/sherlock-project/sherlock) — enumera usernames em 350+ serviços.
- [WhatsMyName](https://whatsmyname.app/) — consulta rápida de usuários em webapps populares.
- [Maigret](https://github.com/soxoj/maigret) — perfis associados a um nickname em mais de 2.000 sites.
- [Holehe](https://github.com/megadose/holehe) — verifica se um e-mail está cadastrado em plataformas.
- [Blackbird](https://github.com/p1ngul1n0/blackbird) — alternativa leve para busca por usuário.
- [Socialscan](https://github.com/iojw/socialscan) — valida disponibilidade de usuários e e-mails.

## Plataformas Específicas
### Twitter / X
- [Twint](https://github.com/twintproject/twint) — coleta tweets, seguidores e interações sem API.
- [snscrape](https://github.com/JustAnotherArchivist/snscrape) — exporta tweets, perfis e hashtags em lotes.
- [TweetBeaver](https://tweetbeaver.com/) — consulta curtidas, listas, seguidores.
- [Bot Sentinel](https://botsentinel.com/) — sinaliza comportamentos inautênticos.

### Instagram
- [Instaloader](https://github.com/instaloader/instaloader) — baixa posts, stories, metadados.
- [OSINTgram](https://github.com/Datalux/Osintgram) — CLI com consultas pré-definidas.
- [Picuki](https://www.picuki.com/) — visualização web anônima de perfis e hashtags.

### LinkedIn
- [RocketReach](https://rocketreach.co/) — enriquecimento de contatos corporativos.
- [Hunter.io](https://hunter.io/) — descobre padrões de e-mail da organização.
- [PhantomBuster](https://phantombuster.com/) — automações para exportar conexões (atenção a limites de uso).

### TikTok
- [TikTok-OSINT](https://github.com/isaacjullien/TikTok-OSINT) — extrai metadados de contas.
- [TikTok-Scraper](https://github.com/drawrowfly/tiktok-scraper) — realiza download em lote de vídeos.
- [Urlebird](https://urlebird.com/) — visualização web sem login.

### Telegram
- [Telegago](https://github.com/Telegago/Telegago) — busca grupos e canais públicos.
- [Telemetr.io](https://telemetr.io/) — analytics de engajamento e crescimento.
- [IntelX Telegram](https://intelx.io/tools?tab=telegram) — pesquisa em histórico preservado.

### Discord
- [Disboard](https://disboard.org/) — diretório de servidores por tópicos.
- [Discord Lookup](https://discord.id/) — converte IDs numéricos em perfis.
- [Snowsta](https://snowsta.com/) — interpreta snowflakes para obter timestamps.

### Outras Redes
- [PeekYou](https://www.peekyou.com/) — agregador de perfis públicos.
- [IDcrawl](https://www.idcrawl.com/) — consolida menções em redes sociais.
- [Search4Faces](https://search4faces.com) — reconhecimento facial focado em VK.

## Boas Práticas de Correlação
- Combine scraping (Twint, Instaloader) com análise manual para validar contexto.
- Armazene capturas em `assets/` com nomes neutros (`case123_doc01.png`).
- Registre fontes, data e confiança utilizando `docs/modelos/dossie-investigativo.md`.

## Alertas de OPSEC
- Utilize VPNs ou identidades de fantoche conforme `docs/Processos/criacao-de-fantoche-sock-puppet.md`.
- Respeite termos de uso das plataformas e evite interações diretas com alvos.
- Teste scripts em ambientes isolados para conter possíveis bloqueios de conta.
