# Checklist OPSEC — Operações de OSINT e Sock Puppets

## Introdução
OPSEC (Operational Security / Segurança Operacional) é o conjunto de práticas que evita que informações críticas da sua **identidade real** sejam expostas durante investigações, infiltrações ou coleta de dados em fontes abertas.  
Este checklist serve como guia rápido para analistas e times de OSINT.

⚠️ **Regra de ouro**: qualquer descuido (um clique errado, uma foto no reflexo, um login no browser errado) pode expor sua identidade real.  
Trabalhe sempre com **isolamento, consistência e disciplina**.

---

## 1. Ambiente Técnico
- [ ] Usar **VMs ou containers** dedicados para investigações (ex: Kali, Tails, Whonix).  
- [ ] Separar ambientes para sock puppets e uso pessoal.  
- [ ] Navegador limpo (sem histórico, extensões pessoais ou cookies).  
- [ ] Bloquear geolocalização, WebRTC e fingerprinting do navegador.  
- [ ] Usar **VPN confiável** e, se possível, encadear com Tor.  
- [ ] Não logar com contas pessoais em ambiente de investigação.  
- [ ] Clock do sistema configurado conforme região da persona.  

---

## 2. Identidade Digital (Sock Puppet)
- [ ] Nome, sobrenome e data de nascimento coerentes.  
- [ ] Endereços e históricos consistentes (sem contradições óbvias).  
- [ ] Uso de e-mails descartáveis ou serviços específicos para sock puppets.  
- [ ] Fotos criadas via **IA** ou bancos de imagens livres (nunca fotos reais).  
- [ ] Postagens e interações compatíveis com o “histórico de vida” da persona.  
- [ ] Nunca misturar persona com contatos reais (amizades, likes, follows).  

---

## 3. Comunicação
- [ ] Usar apps de mensagem isolados em ambientes separados.  
- [ ] Evitar número pessoal (usar VoIP, Burner Phone, SIM anônimo onde legal).  
- [ ] Configurar timezone condizente com a persona.  
- [ ] Redigir mensagens no estilo, idioma e gírias do personagem.  
- [ ] Jamais enviar documentos ou arquivos pessoais pelo sock puppet.  

---

## 4. Comportamento Online
- [ ] Evitar padrões de escrita que revelem sua identidade (estilo, erros típicos).  
- [ ] Variar horários de login e atividade conforme rotina da persona.  
- [ ] Não acessar sites pessoais (banco, e-mail real, redes sociais reais).  
- [ ] Verificar se não há **leak de metadados** em imagens ou documentos enviados.  
- [ ] Simular histórico de navegação da persona (cookies, favoritos, etc.).  

---

## 5. Higiene de Dados
- [ ] Sanitizar prints e evidências (remover metadados antes de salvar/compartilhar).  
- [ ] Guardar evidências em repositório seguro, com controle de acesso.  
- [ ] Usar naming convention que não revele a origem real (ex: `case123_doc01.png`).  
- [ ] Registrar **fonte, data e confiança** de cada evidência coletada.  

---

## 6. Auditoria Pessoal
- [ ] Revisar periodicamente se a persona está **consistente** em todas as plataformas.  
- [ ] Testar se informações cruzadas podem levar à identidade real.  
- [ ] Validar se o sock puppet sobrevive a uma análise básica de OSINT.  
- [ ] Atualizar e “envelhecer” a persona com o tempo (posts, conexões, interações).  

---

## 7. Pós-Operação
- [ ] Encerrar conexões VPN/Tor usadas na operação.  
- [ ] Descartar contas e e-mails descartáveis criados para a missão.  
- [ ] Apagar logs locais e snapshots de VM se não forem necessários.  
- [ ] Armazenar relatórios apenas em repositórios controlados pela equipe.  

---

## Conclusão
OPSEC é uma prática contínua: **não basta criar a persona, é preciso mantê-la viva e segura**.  
Este checklist deve ser usado como guia antes, durante e depois de qualquer operação de OSINT.

---
