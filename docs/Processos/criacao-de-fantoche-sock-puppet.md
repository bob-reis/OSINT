# Criação de Fantoche (Sock Puppet) para OSINT

> Uso exclusivo para fins defensivos, educacionais e de pesquisa autorizada. Respeite leis locais e os Termos de Serviço de cada plataforma.

## Por que usar fantoches em OSINT
- Segurança pessoal e operacional ao investigar alvos sensíveis.
- Evitar levantar suspeitas ou provocar mudança de comportamento do alvo.
- Separar completamente sua pegada digital real das atividades de investigação.
- Permitir coleta imparcial de dados, reduzindo risco reputacional.

## Passo 1 — Ambiente isolado
- Use uma VM por identidade (ex.: VirtualBox/VMware/Proxmox). Nunca use seu SO principal.
- Separe: usuário do sistema, navegador, cache, downloads e pastas (um “mundo” por persona).
- Configure região/idioma/teclado/timezone compatíveis com a persona.
- SO dedicado: considere imagens live ou compartmentalizadas (ex.: Qubes OS, Pop!_OS com criptografia total) para limitar rastros persistentes.
- Navegador: minimize impressão digital (fingerprint) e cookies cruzados; evite extensões pessoais. Prefira instâncias endurecidas (Tor Browser, LibreWolf, Brave em perfil separado).
- Rede: VPN estável; considere Tor apenas se for crível para a persona/uso. Priorize provedores auditados (Proton VPN, Mullvad, IVPN) e registre a rota usada.
- Antes de operar, execute testes não invasivos (BrowserLeaks, CoverYourTracks) para identificar vazamentos de IP, WebRTC ou fingerprint.

## Passo 2 — Insumos de registro
### E‑mail
- Prefira provedores com cadastro simples (ex.: Proton). Combine com a nacionalidade da persona quando fizer sentido (provedor popular no país alvo).
- Padronize padrões de usuário (ex.: `nome.sobrenome123`). Documente as credenciais no dossiê.
- Mantenha uma conta por persona; não reutilize endereços ou aliases entre investigações.

### Telefone
- Opções: número virtual (vida útil limitada) ou SIM físico dedicado (maior longevidade).
- Lembrete: muitas redes exibem parte do número na recuperação de senha — isso “revela” país.
- Evite números vinculados ao seu CPF/identidade real.
- Avalie validade jurídica do serviço (ToS, KYC) e descarte linhas após uso quando previsto pelo plano de OPSEC.

## Passo 3 — Construindo a identidade
### Dados pessoais
- Nome: escolha entre os mais comuns do país alvo (sem ser o #1 óbvio). 
- Data de nascimento: válida e não relacionada à sua. Evite 29/02 em ano não bissexto.
- Verifique combinações com NAMINT: https://seintpl.github.io/NAMINT/
- Registre backstory, rotinas e gatilhos de memória em cofre seguro (Obsidian offline, gerenciador de senhas) para manter consistência.

### Fotos de perfil
- IA (thispersondoesnotexist.com/geradores): realistas, porém detectáveis por padrões.
- Objetos/abstratas (carro, flores): reduzem riscos de reconhecimento facial.
- “Doadores” inativos: apenas se não houver PII/localização explícita; faça variações.
- Edite/remova EXIF de imagens. Mantenha a coerência com interesses do perfil.

## Passo 4 — Tornando a conta crível
### Localização e emprego
- Endereço deve existir. Siga grupos locais para “sinais” de contexto.
- Emprego: organizações grandes e discretas. Título de cargo plausível.

### Interesses e atividades
- Selecione interesses comuns e que você domine ao menos o básico.
- Publique e interaja gradualmente (aquecimento): curtidas/comentários espaçados por dias/semanas.
- Planeje cadência de conteúdo (posts leves, compartilhamentos, check-ins) coerente com a persona.
- Documente interações relevantes no dossiê para repetir padrões quando necessário.

### Conexões
- Busque conexões em grupos locais e de interesse. Não precisa “centenas”; o suficiente para parecer normal.
- Para comunidades fechadas, combine presença prévia com convites plausíveis antes de engajar o alvo.

## Boas práticas de OPSEC
- Nunca misture infra: VM, navegador, contas e telefone da persona não cruzam com os seus.
- Sanitize tudo: metadados, prints, nomes de arquivos (`case123_doc01.png`).
- Use senhas fortes e únicas; considere gerenciador e 2FA compatível com o isolamento.
- Registre “histórico” coerente: datas de criação, primeiros posts e grupos devem contar uma história.
- Faça “health checks” periódicos: a persona resiste a uma busca OSINT básica? Avalie com scans de fingerprint e reputação.
- Mantenha logs mínimos, apagando snapshots ou notas fora do cofre seguro quando concluído.

## Relacionados neste repositório
- Checklist de criação: `checklists/checklist-criacao-sock-puppet.md`
- Template de dossiê investigativo: `docs/modelos/dossie-investigativo.md`

## Resumo
Fantoches bem‑construídos imitam perfis comuns, com identidade consistente, sinais locais, interesses plausíveis e atividade gradual. O pilar é o isolamento operacional absoluto: nada conecta a persona a você, e cada passo deve ser monitorado com verificações periódicas de exposição.
