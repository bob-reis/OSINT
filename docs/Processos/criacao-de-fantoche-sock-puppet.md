# Criação de Fantoche (Sock Puppet) para OSINT

> Uso exclusivo para fins defensivos, educacionais e de pesquisa autorizada. Respeite leis locais e os Termos de Serviço de cada plataforma.

## Por que usar fantoches em OSINT
- Segurança pessoal e operacional ao investigar alvos sensíveis.
- Evitar levantar suspeitas ou provocar mudança de comportamento do alvo.
- Separar completamente sua pegada digital real das atividades de investigação.

## Passo 1 — Ambiente isolado
- Use uma VM por identidade (ex.: VirtualBox/VMware/Proxmox). Nunca use seu SO principal.
- Separe: usuário do sistema, navegador, cache, downloads e pastas (um “mundo” por persona).
- Configure região/idioma/teclado/timezone compatíveis com a persona.
- Navegador: minimize impressão digital (fingerprint) e cookies cruzados; evite extensões pessoais.
- Rede: VPN estável; considere Tor apenas se for crível para a persona/uso.

## Passo 2 — Insumos de registro
### E‑mail
- Prefira provedores com cadastro simples (ex.: Proton). Combine com a nacionalidade da persona quando fizer sentido (provedor popular no país alvo).
- Padronize padrões de usuário (ex.: `nome.sobrenome123`). Documente as credenciais no dossiê.

### Telefone
- Opções: número virtual (vida útil limitada) ou SIM físico dedicado (maior longevidade).
- Lembrete: muitas redes exibem parte do número na recuperação de senha — isso “revela” país.
- Evite números vinculados ao seu CPF/identidade real.

## Passo 3 — Construindo a identidade
### Dados pessoais
- Nome: escolha entre os mais comuns do país alvo (sem ser o #1 óbvio). 
- Data de nascimento: válida e não relacionada à sua. Evite 29/02 em ano não bissexto.
- Verifique combinações com NAMINT: https://seintpl.github.io/NAMINT/

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

### Conexões
- Busque conexões em grupos locais e de interesse. Não precisa “centenas”; o suficiente para parecer normal.

## Boas práticas de OPSEC
- Nunca misture infra: VM, navegador, contas e telefone da persona não cruzam com os seus.
- Sanitize tudo: metadados, prints, nomes de arquivos (`case123_doc01.png`).
- Use senhas fortes e únicas; considere gerenciador e 2FA compatível com o isolamento.
- Registre “histórico” coerente: datas de criação, primeiros posts e grupos devem contar uma história.
- Faça “health checks” periódicos: a persona resiste a uma busca OSINT básica?

## Relacionados neste repositório
- Checklist de criação: `checklists/checklist-criacao-sock-puppet.md`
- Template de dossiê investigativo: `docs/modelos/dossie-investigativo.md`

## Resumo
Fantoches bem‑construídos imitam perfis comuns, com identidade consistente, sinais locais, interesses plausíveis e atividade gradual. O pilar é o isolamento operacional absoluto: nada conecta a persona a você.

