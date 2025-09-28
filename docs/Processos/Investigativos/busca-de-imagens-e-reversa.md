# Busca de Imagens e Pesquisa Reversa

## Objetivo
Identificar origem, versões e autenticidade de imagens coletadas durante investigações, cruzando metadados, histórico e possíveis manipulações.

## Preparação Rápida
1. Salve cópia original da imagem e gere hash SHA-256 para controle de integridade.
2. Remova dados sensíveis antes de compartilhar com terceiros.
3. Planeje consultas multiplataforma (Google, Yandex, Bing) para ampliar cobertura.

## Motores de Pesquisa Reversa
- [Google Imagens](https://images.google.com/) — comparação visual e domínios associados.
- [Yandex Imagens](https://yandex.com/images/) — destaque para reconhecimento facial e objetos.
- [Bing Visual Search](https://www.bing.com/visualsearch) — sugere entidades e produtos similares.
- [TinEye](https://tineye.com/) — histórico de versões mais antigas.
- [Karma Decay](https://karmadecay.com/) — foco em conteúdo publicado no Reddit.

## Extração de Metadados
- [ExifTool](https://exiftool.org/) — CLI robusta para EXIF, IPTC e XMP.
- [Jeffrey’s EXIF Viewer](http://exif.regex.info/exif.cgi) — análise rápida no navegador.
- [metapicz](https://www.metapicz.com/#landing) — visualização estruturada de metadados.

## Análise Forense
- [Forensically](https://29a.ch/photo-forensics/) — ELA, clone detection e magnifier.
- [FotoForensics](http://fotoforensics.com/) — erro de compressão e histogramas.
- [ImageEdited?](https://imageedited.com/) — validações automatizadas de edição.

## Reconhecimento Facial
- [PimEyes](https://pimeyes.com/) — busca comercial por correspondências faciais.
- [FindClone](https://findclone.ru/) — motor russo com alta taxa de acerto (atentar a leis locais).
- [Search4Faces](https://search4faces.com/) — cruzamento específico com VKontakte.

## Boas Práticas
- Compare resultados de diferentes motores para evitar vieses regionais.
- Utilize metadados apenas como indicativos; valide com outras evidências.
- Documente cada passo (URL, data, confiança) no dossiê investigativo.

## Alertas de OPSEC
- Evite upload de imagens sensíveis em serviços públicos sem ofuscação.
- Utilize intermediários (cURL, VMs) para reduzir pegada pessoal.
- Respeite legislação e políticas de privacidade ao usar reconhecimento facial.
