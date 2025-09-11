# OSINT no Telegram — Você não se esconde

> Uso exclusivo para fins defensivos, educacionais e de pesquisa autorizada. Respeite leis e Termos de Serviço.

## Contexto
Telegram ganhou relevância (ex.: guerra Rússia-Ucrânia) e concentra grande volume de informação. Embora ofereça boas opções de privacidade, usuários, canais e grupos deixam sinais úteis para OSINT.

## Identificadores no Telegram
- ID Telegram: numérico, único e imutável (não muda com nome/telefone). Bots de utilidade podem revelar o ID a partir de @username/canal.
- Nome de exibição: livre, não único. Útil só com contexto.
- @username: único e reutilizável; pode mudar. Verifique:
  - Acesso direto: `https://t.me/USERNAME`
  - Dork: `site:t.me "USERNAME"`
  - Pesquisa reversa de username: https://whatsmyname.app
- Data de criação: alguns bots retornam a partir de mensagens encaminhadas (ex.: CreationDateBot).

## Verificação e deanonimização
- Inspecione perfil: foto, nome exibido, @username, bio e links.
- Valide cada item de forma independente e correlacione depois.
- Foto: busca reversa (Google/Yandex), verifique EXIF/indícios no fundo; compare com suposta localização.
- Consistência: idioma, fuso/horário de posts, gírias, interesses, padrões do dispositivo.
- Atenção legal/ética ao usar bots agregadores de vazamentos (ex.: OsintKit, Eye of God, Horus). Disponibilidade varia e pode violar ToS.

## Atividade e grupos
- Dentro de grupos: use “pesquisar mensagens de” para mapear comportamento, interesses e horários.
- Descobrir grupos de um usuário (serviços de terceiros, muitas vezes pagos):
  - TelegramDB (web/bot): busca por grupos e, pago, grupos onde o usuário esteve.
  - TGScan: base ampla; mostra última atividade em grupos.
  - Where a Person Wrote Bot: gratuito, base menor.
- Dica: relações com chats de cidade/temas revelam localidade/interesses.

## Busca de informação (canais/grupos)
- Busca interna: funciona bem em canais/grupos já assinados; crie conta separada por tema para organizar.
- Google dorks:
  - Tudo/onde: `site:t.me/* ("termo1" OR "termo2")`
  - Convides únicos: `"https://t.me/+RANDOMSTRING"` (entre aspas)
  - Título do canal/chat: `site:t.me/* intitle:osint`
- Buscadores (Google CSE):
  - Telegago: `https://cse.google.com/cse?&cx=006368593537057042503:efxu7xprihg`
  - Alternativa CSE: `https://cse.google.com/cse?cx=004805129374225513871:p8lhfo0g3hg`
  - Tgfind: `https://tgfind.org/` (busca em período de tempo)
- Catálogos/analíticos:
  - Telemetr.io: estatísticas, busca por nome/país, posts (inclui alguns deletados na versão paga/grátis 7 dias).

## Arquivo e conteúdo deletado
- Wayback Machine arquiva Telegram desde 2022 (coleção dedicada). Como usar:
  1) Pesquise termo/frase na página principal;
  2) Em “Collection Search”, selecione a coleção Telegram;
  3) Abra snapshots e links originais quando disponíveis.
- Limitações: nem sempre salva mídias; exige paciência.

## Boas práticas
- Defina objetivo, hipótese e termos antes de buscar.
- Registre fontes, datas e confiança (use `docs/modelos/dossie-investigativo.md`).
- Respeite privacidade/lei; não contorne controles de acesso.

