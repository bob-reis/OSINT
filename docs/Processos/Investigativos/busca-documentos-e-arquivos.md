# Busca de Documentos e Arquivos

## Objetivo
Localizar documentos, apresentações e arquivos hospedados publicamente para extrair metadados, evidências e referências.

## Preparação Rápida
1. Determine formatos-alvo (`filetype:pdf`, `ext:ppt`) e temas chave.
2. Verifique restrições legais antes de baixar conteúdo potencialmente sensível.
3. Organize armazenamento em `assets/` com nomes neutros.

## Motores Focados em Documentos
- [FindPDFDoc](http://www.findpdfdoc.com/) — busca dedicada a PDFs, DOCs e apresentações.
- [SlideShare](https://www.slideshare.net/) — apresentações corporativas e acadêmicas.
- [Scribd](https://www.scribd.com/) — acervo de livros, relatórios e apostilas.
- [DocJax](https://docjax.com) — buscador de documentos com filtros rápidos.

## Diretórios e Arquivos Expostos
- [FilePursuit](https://filepursuit.com/) — indexa diretórios abertos e servidores.
- [Eyedex](http://eyedex.org/) — busca arquivos em diretórios públicos.
- [Filesec.io](https://filesec.io/) — foco em conteúdo de infosec.
- [Meawfy](https://meawfy.com/) — pesquisa arquivos hospedados no Mega.

## Pastes e Armazenamento de Texto
- [0bin](https://0bin.net/) — pastes criptografados client-side.
- [Cryptobin](https://cryptobin.co/) — armazenamento seguro temporário.
- [Defuse Pastebin](https://defuse.ca/pastebin.htm) — inclui opção de expiração e criptografia.

## Boas Práticas
- Extraia metadados com `exiftool` ou `docs/Processos/osint_darkweb_doc.md` como referência.
- Mantenha registro de hashes e fontes para validar integridade.
- Use operadores combinados (`site:gov filetype:xls`) para consultas mais precisas.

## Alertas de OPSEC
- Evite baixar arquivos executáveis em ambientes de produção.
- Analise documentos suspeitos em sandbox (VM) antes de abrir.
- Respeite direitos autorais ao armazenar ou compartilhar os materiais coletados.
