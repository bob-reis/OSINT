# Checklist — Criação de Persona (Sock Puppet) para OSINT

> Uso exclusivamente defensivo, educacional e de pesquisa autorizada. Respeite leis locais e Termos de Serviço das plataformas.

## 1. Preparação Inicial
- [ ] Definir objetivo da persona (ex: infiltração em grupo X, observação de rede social Y).  
- [ ] Escolher nome, data de nascimento e histórico coerente (usar geradores de identidade/fake ID).  
- [ ] Criar e-mail seguro (Proton, Tutanota, RiseUp), alinhado ao país da persona quando fizer sentido.  
- [ ] Configurar VM/container dedicado — idealmente uma VM por persona; nunca usar o SO pessoal.  
- [ ] Avaliar uso de SO/ambiente orientado à privacidade (ex.: Qubes OS, Pop!_OS com criptografia total).  
- [ ] Selecionar navegador endurecido (Tor Browser, LibreWolf, Brave) em perfil exclusivo para a persona.  
- [ ] Ajustar idioma/teclado/timezone/localização da VM conforme a persona.  
- [ ] Aplicar VPN estável; considerar Tor somente se crível para o contexto.  
- [ ] Validar ambiente com testes não invasivos (BrowserLeaks, CoverYourTracks) antes da primeira operação.  
- [ ] Definir gerenciador de senhas e 2FA compatíveis com o isolamento.  
- [ ] Iniciar dossiê da persona (credenciais, datas, padrões) em `docs/modelos/dossie-investigativo.md`.  

---

## 2. Identidade Básica
- [ ] Nome completo definido.  
- [ ] Apelidos e alias consistentes.  
- [ ] Endereço fictício (usando mapas reais, mas sem expor locais próprios).  
- [ ] Histórico escolar plausível.  
- [ ] Profissão/ocupação atual compatível com idade e trajetória.  
- [ ] Idiomas e gírias condizentes.  

---

## 3. Identidade Digital
- [ ] Criar redes sociais coerentes (Facebook, LinkedIn, Instagram, Twitter/X).  
- [ ] Verificar nomes/aliases com NAMINT e disponibilidade de @usuários.  
- [ ] Gerar fotos falsas (IA/geradores) ou usar objetos/abstratas; sempre remover EXIF.  
- [ ] Aquecer a conta gradualmente (curtidas/comentários/seguidas ao longo de dias/semanas).  
- [ ] Planejar cadência de conteúdo e interações críveis para a persona.  
- [ ] Interagir em fóruns/grupos condizentes com o perfil.  
- [ ] Usar padrões de escrita e horários compatíveis com a persona.  

---

## 4. Comunicação
- [ ] Número descartável (VoIP, Burner SIM, aplicativos de segundo número).  
- [ ] Ciente: recuperação de senha pode exibir parte do número (indício de país).  
- [ ] Configurar apps de mensagem isolados (Signal, Telegram, Wickr) sem sincronizar contatos.  
- [ ] Ajustar idioma e estilo de comunicação.  
- [ ] Nunca cruzar sock puppet com contatos reais.  

---

## 5. Movimentação Financeira (opcional e contextual)
- [ ] Criar carteiras apenas quando necessário ao cenário/credibilidade.  
- [ ] Simular histórico com cautela (testnet/faucets ou quantias mínimas).  
- [ ] Preferir soluções legais e conformes; evite qualquer violação de KYC/AML.  
- [ ] Documentar claramente a finalidade e o contexto no dossiê.  

---

## 6. Aparência / Sinais
- [ ] Cor do cabelo, altura, peso e estilo definidos.  
- [ ] Fotos ajustadas com EXIF limpo (sem metadados).  
- [ ] Estilo de roupa coerente com idade e profissão da persona.  
- [ ] Presença digital coerente com hobbies, esportes ou crenças.  

---

## 7. Familiares e Rede Social
- [ ] Definir estado civil.  
- [ ] Criar ou simular parceiro(a), irmãos, amigos (pode usar outras personas).  
- [ ] Simular rede mínima de conexões (curtidas, interações básicas).  
- [ ] Nunca usar dados de pessoas reais próximas a você.  

---

## 8. OPSEC e Higiene
- [ ] Nunca logar sock puppet em máquina pessoal.  
- [ ] Registrar backstory, credenciais e interações em cofre isolado para evitar contradições.  
- [ ] Revisar consistência de todas as informações.  
- [ ] Sanitizar prints e arquivos antes de armazenar.  
- [ ] Usar convenção de nomes neutros para evidências (`case123_img01.png`).  
- [ ] Minimizar fingerprint do navegador (idioma/UA/fusos/fontes coerentes).  
- [ ] Manter segregação de infra (VM, contas, telefones dedicados).  
- [ ] Revisar se a persona sobrevive a uma análise de OSINT básica.  

---

## 9. Pós-Operação
- [ ] Encerrar conexões (VPN/Tor).  
- [ ] Desativar recuperações desnecessárias (e‑mail/telefone) e revisar segurança.  
- [ ] Deletar ou arquivar contas descartáveis conforme política do caso.  
- [ ] Apagar logs/snapshots de VM se não forem necessários.  
- [ ] Guardar relatório e cadeia de custódia de forma segura.  
