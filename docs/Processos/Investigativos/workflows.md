# OSINT Workflows (repo privado)

Guia visual de fluxos OSINT para **Google Dorks, Domínio, E-mail, Localização, Nome Real, Telefone e Username**.
Cada diagrama foi otimizado para leitura no GitHub (vertical e compacto).

> **✨ Novo**: Adicionado fluxo completo para **Google Dorks** com 7 categorias de busca e workflow de disclosure responsável.

## Índice
- [Fluxo: Google Dorks](#fluxo-google-dorks) ⭐ **NOVO!**
- [Fluxo: Domain Name](#fluxo-domain-name)
- [Fluxo: Email Address](#fluxo-email-address)
- [Fluxo: Location](#fluxo-location)
- [Fluxo: Real Name](#fluxo-real-name)
- [Fluxo: Telephone](#fluxo-telephone)
- [Fluxo: Username](#fluxo-username)
- [🧅 Recursos Dark Web/Onion](#recursos-dark-webonion) ⭐ **NOVO!**

---

## Fluxo: Google Dorks
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["🎯 Alvo Definido<br/>(Domínio/Empresa)"]

    %% Preparação
    subgraph S1 ["🛡️ Preparação OPSEC"]
        B1["VPN/Tor Ativo"]
        B2["VM Isolada"]
        B3["Autorização Obtida"]
        B4["Escopo Definido"]
    end

    %% Categorias de Dorks
    subgraph S2 ["📁 Arquivos de Configuração"]
        C1["site:target.com ext:conf"]
        C2["site:target.com ext:env"]
        C3["site:target.com ext:ini"]
        C4["inurl:config.php"]
        C5["inurl:wp-config.php"]
    end

    subgraph S3 ["💾 Backups & Databases"]
        D1["site:target.com ext:bak"]
        D2["site:target.com ext:backup"]
        D3["site:target.com ext:sql"]
        D4["inurl:backup.zip"]
        D5["inurl:dump.sql"]
    end

    subgraph S4 ["🔐 Painéis Admin"]
        E1["site:target.com inurl:admin"]
        E2["site:target.com inurl:login"]
        E3["intitle:'Admin Panel'"]
        E4["inurl:wp-admin"]
        E5["inurl:cpanel"]
    end

    subgraph S5 ["🌐 APIs & Endpoints"]
        F1["site:target.com inurl:api"]
        F2["site:target.com inurl:rest"]
        F3["site:target.com inurl:graphql"]
        F4["inurl:/v1/ | inurl:/v2/"]
        F5["inurl:swagger"]
    end

    subgraph S6 ["🔑 Credenciais & Secrets"]
        G1["site:target.com intext:password"]
        G2["intext:api_key"]
        G3["intext:aws_access_key"]
        G4["intext:github_token"]
        G5["filetype:env SECRET"]
    end

    subgraph S7 ["📋 Documentos Sensíveis"]
        H1["site:target.com ext:pdf"]
        H2["site:target.com ext:docx"]
        H3["intext:'confidencial'"]
        H4["ext:xls password"]
        H5["filetype:log"]
    end

    %% Análise e Validação
    subgraph S8 ["🔍 Análise de Resultados"]
        I1["Filtrar Falsos Positivos"]
        I2["Validar Exposições"]
        I3["Classificar Criticidade"]
        I4["Documentar Achados"]
    end

    %% Ações
    subgraph S9 ["⚡ Ações Responsáveis"]
        J1["Disclosure Responsável"]
        J2["Relatório Técnico"]
        J3["Evidências Censuradas"]
        J4["Timeline de Correção"]
    end

    %% Fluxo principal
    A --> B1
    A --> B2
    A --> B3
    A --> B4

    B1 --> C1
    B2 --> D1
    B3 --> E1
    B4 --> F1

    C1 --> C2
    C2 --> C3
    C3 --> C4
    C4 --> C5

    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> D5

    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 --> E5

    F1 --> F2
    F2 --> F3
    F3 --> F4
    F4 --> F5

    G1 --> G2
    G2 --> G3
    G3 --> G4
    G4 --> G5

    H1 --> H2
    H2 --> H3
    H3 --> H4
    H4 --> H5

    %% Convergência para análise
    C5 --> I1
    D5 --> I1
    E5 --> I2
    F5 --> I2
    G5 --> I3
    H5 --> I3

    I1 --> I4
    I2 --> I4
    I3 --> I4

    I4 --> J1
    J1 --> J2
    J2 --> J3
    J3 --> J4

    %% Especialização por CMS
    E4 --> WP["WordPress Dorks"]
    WP --> WP1["inurl:wp-content/"]
    WP --> WP2["inurl:wp-includes/"]
    WP --> WP3["filetype:sql wp-content"]

    %% Cloud & Infra
    G3 --> AWS["AWS Secrets"]
    AWS --> AWS1["s3.amazonaws.com"]
    AWS --> AWS2["intext:bucket"]
    AWS --> AWS3["filetype:json aws"]
```

**📖 Guia de Uso do Fluxo:**

1. **🛡️ Preparação OPSEC**: Sempre configure ambiente seguro antes de iniciar
2. **🎯 Definição de Escopo**: Use `site:target.com` para manter foco
3. **📂 Execução Sistemática**: Percorra cada categoria metodicamente
4. **🔍 Validação**: Confirme exposições antes de relatar
5. **⚖️ Disclosure Ético**: Reporte vulnerabilidades responsavelmente

**🚨 Lembretes Importantes:**
- ✅ Sempre obtenha autorização por escrito
- ✅ Mantenha logs de atividades
- ✅ Censure dados sensíveis em evidências
- ❌ Nunca acesse sistemas sem permissão
- ❌ Não baixe dados pessoais/confidenciais

**📚 Referência Completa**: [Google Dorks - Guia Completo](google-dorks-guia-completo.md)

---

## Fluxo: Domain Name
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["Domain Name"]

    %% Live website & engines
    subgraph S1 ["Live Website & Engines"]
      B["Live Website"]
      I["Google"]
      J["Bing"]
      K["Yandex"]
      L["Wayback Machine"]
      M["Cached"]
      N["site: Search"]
      O["IntelTechniques Domain Search Tool"]
    end

    %% Analytics
    subgraph S2 ["Analytics"]
      C1["SpyOnWeb"]
      C2["DomainCrawler"]
      C3["AnalyzeID"]
      C4["NerdyData"]
      C5["PubDB"]
    end

    %% Domain/Whois/History
    subgraph S3 ["Domain / WHOIS / History"]
      U["Domain History"]
      V["Whoisology"]
      W["Who.is"]
      X["WhoisInfo"]
      Y["ViewDNS Whois"]
      Z["WhoisMind"]
      AA["Who.is History"]
      AB["DNSTrails"]
      AC["ViewDNS-IP"]
      AD["ViewDNSHistory"]
      AE["Backlinks"]
      AF["SharedCount"]
      AG["Robots.txt"]
      AH["Hidden Pages"]
    end

    %% FOCA
    subgraph S4 ["FOCA Extraction"]
      P["Real Name"]
      Q["Email Address"]
      R["Documents"]
      S["IP Address"]
      T["Social Networks"]
    end

    %% Infra & Pentest
    subgraph S5 ["Infra & Pentest"]
      D["New Domains"]
      E["Pentest Tools"]
      F["Sub Domains"]
      H["App: Metagoofil"]
    end

    A --> B
    A --> C1
    A --> P
    A --> D

    B --> I
    B --> J
    B --> K
    B --> L
    I --> M
    J --> M
    K --> M
    L --> M
    M --> N
    N --> O
    O --> U
    O --> V
    O --> W
    O --> X
    O --> Y
    O --> Z
    O --> AA
    O --> AB
    O --> AC
    O --> AD
    O --> AE
    O --> AF
    O --> AG
    O --> AH

    C5 --> P
    E --> F
    F --> H
    T --> AI["Small SEO Tools"]

    %% Integração com Google Dorks
    A --> GD["🔍 Google Dorks"]
    GD --> GD1["site:domain.com ext:conf"]
    GD --> GD2["site:domain.com inurl:admin"]
    GD --> GD3["site:domain.com ext:bak"]
    GD1 --> U
    GD2 --> E
    GD3 --> AB
```

**💡 Dica**: Para uma investigação mais completa do domínio, use também o [Fluxo: Google Dorks](#fluxo-google-dorks) com foco específico no `site:dominio.com`.

---

## Fluxo: Email Address
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["Email Address"]

    A --> B["Verify address - Hunter.io"]
    A --> C["Remove domain and search username"]
    A --> D["Search Facebook by email"]
    A --> E["Document search"]
    A --> F["Pipl API"]
    A --> G["Email search tool - IntelTechniques"]

    %% Search engines
    subgraph S1 ["Search engines"]
      H1["Google"]
      H2["Yandex"]
      H3["Bing"]
    end
    B --> S1
    S1 --> H4["Websites / Blogs"]

    %% Breaches
    subgraph S2 ["Compromised databases"]
      I1["HIBP"]
      I2["Hacked-Emails"]
    end
    B --> S2

    %% Username
    C --> J["User name"]
    H4 --> J

    %% Resultados
    D --> K["Employer"]
    E --> L["Real name"]

    %% People/email services
    subgraph S3 ["People / email services"]
      N1["Pipl"]
      N2["ThatsThem"]
      N3["ReverseMails"]
      N4["Newsgroups"]
      N5["DomainData"]
      N6["Gravatar"]
    end
    G --> N1
    G --> N2
    G --> N3
    G --> N4
    G --> N5
    G --> N6

    %% Social
    N1 --> R["Social networks"]
    N2 --> R
    N3 --> R
    N4 --> R
    N5 --> R
    N6 --> R
    S2 --> R
    D --> R
    F --> R
    G --> R

    %% Expansão por username
    J --> O["Search engines"]
    J --> P["Email permutator"]
    J --> Q["Email search engines"]
    Q --> R

    %% Assumptions
    R --> S["Email assumptions - work"]
    R --> T["Email assumptions - personal"]

    %% Provedores e FB reset
    P --> U["Gmail / Yahoo / Hotmail"]
    U --> V["Facebook profile"]
    V --> W["FB password reset"]
```

---

## Fluxo: Location
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["Location"]

    A --> B["GPS coordinates"]
    A --> C["IntelTechniques custom maps tool"]
    A --> D["Physical address"]
    A --> E["Search engines"]
    A --> F["Social networks"]

    B --> B1["Twitter"]
    B --> B2["Echosec"]

    E --> G["Google Earth app"]
    E --> H["Historic satellite view"]
    E --> I["Websites / Blogs"]

    subgraph S2 ["Satellite / Street imagery"]
      S2a["LandViewer"]
      S2b["TerraServer"]
      S2c["Zoom Earth"]
      S2d["Yandex Maps"]
      S2e["Descartes"]
      S2f["Google Maps"]
      S2g["Bing Maps"]
      S2h["Mapillary"]
      S2i["Open Street Cams"]
      S2j["Zillow"]
    end
    C --> S2
    S2 --> J["Interior images"]

    subgraph S3 ["People directories"]
      P1["Pipl"]
      P2["Nuwber"]
      P3["ThatsThem"]
      P4["FastPeople"]
    end
    D --> S3
    S3 --> T["Telephone"]

    F --> K["User name"]
    F --> L["Real name"]
    J --> L

    K --> F
    F --> M["New locations"]
    M --> B
    B --> N["Android emulator"]
    N --> O["GPS spoofing"]
    O --> P["Mobile apps"]
```

---

## Fluxo: Real Name
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["Real Name"]

    A --> TW["Twitter"]
    TW --> T1["Who Is Search"]
    TW --> T2["Twitter Posts"]

    A --> FB["Facebook"]
    FB --> FBR["Facebook Password Reset"]
    FB --> FBP["Facebook Profile"]
    FBR --> FBP
    FBP --> UN["User name"]
    UN --> UNUM["User number"]
    UNUM --> FBT["FB custom tools"]
    FBT --> CMT["Comments"]
    FBT --> PHO["Photos"]
    FBT --> VID["Videos"]
    FBT --> EVT["Events"]
    CMT --> SNS["Social networks"]
    PHO --> SNS
    VID --> SNS
    EVT --> SNS

    subgraph PSE ["People search engines"]
      PIPL["Pipl"]
      TT["ThatsThem"]
      AC["AdvCheck"]
      FP["FastPeople"]
      TP["TruePeople"]
      FTN["FamilyTreeNow"]
      INT["Intelius"]
      SPOK["Spokeo"]
    end
    A --> PSE

    PSE --> ADR["Address"]
    PSE --> PHN["Phone #"]
    PSE --> UN2["User name"]
    RES["Resumes"]
    PSE --> RES
    RES --> ADR
    RES --> PHN

    subgraph SE ["Search engines"]
      G["Google"]
      B["Bing"]
      Y["Yandex"]
    end
    A --> SE
    SE --> ADR
    SE --> PHN
    SE --> UN3["User name"]

    ADR --> VR["Voter records"]

    ADR --> IT["Name Search Tool - IntelTechniques"]
    PHN --> IT
    UN2 --> IT
    UN3 --> IT
    IT --> REL["Relatives"]
```

---

## Fluxo: Telephone
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["Telephone #"]

    A --> FB["Facebook search"]
    FB --> FBP["Facebook page"]
    FBP --> FPOST["Facebook posts"]
    FPOST --> SNS1["Social networks"]

    A --> RCW0["Reverse caller ID websites"]
    subgraph RCW ["Reverse websites"]
      RCW0 --> Nuw["Nuwber"]
      RCW0 --> CIDT["CallerIDTest"]
    end

    A --> RCAPI0["Reverse caller ID APIs"]
    subgraph RCAPI ["APIs"]
      RCAPI0 --> Next["NextCaller"]
      RCAPI0 --> OpenC["OpenCNAM"]
      RCAPI0 --> CIDServ["CallerIDService"]
    end

    A --> SRV0["Caller ID services"]
    subgraph SRV ["Services"]
      SRV0 --> Twilio["Twilio"]
      SRV0 --> OpenC2["OpenCNAM"]
      SRV0 --> WhoCall["WhoCallId"]
      SRV0 --> PrivStar["PrivacyStar"]
    end

    RCW0 --> RN["Real name"]
    RCAPI0 --> RN
    Twilio --> RN
    OpenC2 --> RN
    WhoCall --> RN
    PrivStar --> RN
    RN --> SNS2["Social networks"]

    A --> AE["Android emulator"]
    AE --> CT["Contacts"]
    CT --> Gc["Google Custom"]
    Gc --> RADDR["Real address"]
    Gc --> BUS["Business"]

    A --> MOB["Mobile apps"]
    MOB --> FF["Find friends"]
    FF --> PrivStar
    MOB --> UN["User names"]
    UN --> SNS3["Social networks"]

    A --> PPL0["People search by phone"]
    subgraph PPL ["Directories / services"]
      PPL0 --> FPS["FastPeopleSearch"]
      PPL0 --> TPS["TruePeopleSearch"]
      PPL0 --> Pipl411["Pipl / 411"]
      PPL0 --> TrueCaller["True Caller"]
      PPL0 --> TT["ThatsThem"]
      PPL0 --> SyncMe["Sync.me"]
      PPL0 --> WPPlus["WP Plus"]
    end
    PPL0 --> NAME["Name"]

    A --> IT["Number Search Tool - IntelTechniques"]
    IT --> NAME
    IT --> REL["Relatives"]

    SNS1 --> OUT["Social networks (aggregate)"]
    SNS2 --> OUT
    SNS3 --> OUT
    NAME --> OUT
    RADDR --> OUT
    BUS --> OUT
    REL --> OUT
```

---

## Fluxo: Username
[🔝 voltar ao índice](#índice)

```mermaid
flowchart TB
    A["User name"]

    subgraph SE ["Search engines"]
      G["Google"]
      B["Bing"]
      Y["Yandex"]
    end
    A --> SE

    subgraph UST ["Username search tools"]
      K["Knowem"]
      CU["CheckUsernames"]
      NV["NameVine"]
      USH["UserSherlock"]
      USE["UserSearch"]
      PY["PeekYou"]
      PIPL["Pipl"]
    end
    A --> UST

    A --> PEA["Potential email addresses"]
    subgraph DOMS ["Common email domains"]
      D1["x@gmail.com"]
      D2["x@yahoo.com"]
      D3["x@outlook.com"]
      D4["x@live.com"]
      D5["x@hushmail.com"]
      D6["x@mail.com"]
      D7["x@facebook.com"]
    end
    PEA --> DOMS
    DOMS --> EADDR["Email address"]

    A --> ASSU["Email assumptions"]
    ASSU --> HIBP["Have I Been Pwned"]
    ASSU --> HE["Hacked-Emails"]
    HIBP --> EADDR
    HE --> EADDR

    subgraph API ["API searches"]
      AP1["Pipl"]
      AP2["HIBP"]
      AP3["Hacked-Emails"]
      AP4["FullContact"]
    end
    EADDR --> API

    subgraph MAN ["Manual attempts"]
      TW["Twitter"]
      IG["Instagram"]
      FB["Facebook"]
      YT["YouTube"]
    end
    A --> MAN

    IA["Internet archives"]
    SE --> IA

    SN["Social networks"]
    SE --> SN
    UST --> SN
    API --> SN
    MAN --> SN
    IA --> SN

---

## Recursos Dark Web/Onion
[🔝 voltar ao índice](#índice)

### 🧅 Fluxo de Investigação na Dark Web

```mermaid
flowchart TB
    A["🎯 Alvo/POI Identificado"]

    %% Preparação OPSEC
    subgraph S1 ["🛡️ Preparação OPSEC Avançada"]
        B1["VPN Multi-Hop + Tor"]
        B2["VM Isolada (Tails/Whonix)"]
        B3["Autorização Legal Obtida"]
        B4["Sock Puppet Preparado"]
        B5["Documentação Segura"]
    end

    %% Catálogos e Diretórios
    subgraph S2 ["🗂️ Catálogos e Diretórios"]
        C1["Hidden Wiki"]
        C2["Just Onion"]
        C3["Top Onions"]
        C4["Onion Dir"]
        C5["CheckItOnion"]
        C6["Tor Yellow Pages"]
    end

    %% Motores de Busca Dark Web
    subgraph S3 ["🔍 Motores de Busca Especializados"]
        D1["Ahmia.fi"]
        D2["Torch"]
        D3["Haystak"]
        D4["DarkSearch"]
        D5["OnionSearch Tool"]
        D6["Katana"]
    end

    %% Análise por Tipo de Conteúdo
    subgraph S4 ["📊 Análise por Categoria"]
        E1["Fóruns por Região 🌍"]
        E2["Chats Anônimos 💬"]
        E3["Pastebins 📋"]
        E4["Imageboards 📸"]
        E5["Marketplaces 🛒"]
        E6["Mídia/News 📰"]
    end

    %% Fóruns Regionais
    subgraph S5 ["🇷🇺🇫🇷🇩🇪🇹🇷🇧🇷 Fóruns Regionais"]
        F1["Verified Forum (RU)"]
        F2["French World (FR)"]
        F3["Germania (DE)"]
        F4["Shadow Forum (TR)"]
        F5["Respostas Ocultas (BR)"]
        F6["Dread (Global)"]
    end

    %% Ferramentas de Análise
    subgraph S6 ["🔧 Ferramentas de Análise"]
        G1["OnionScan"]
        G2["TorBot"]
        G3["VigilantOnion"]
        G4["Onioff"]
        G5["DeepDarkCTI"]
        G6["Darksearch Tools"]
    end

    %% Coleta e Análise
    subgraph S7 ["📝 Coleta e Documentação"]
        H1["Screenshots Censurados"]
        H2["Metadados de Links"]
        H3["Análise de Disponibilidade"]
        H4["Mapping de Comunidades"]
        H5["Timeline de Atividades"]
    end

    %% Threat Intelligence
    subgraph S8 ["🚨 Threat Intelligence"]
        I1["IOCs Extraction"]
        I2["TTPs Mapping"]
        I3["Ransomware Groups"]
        I4["Threat Actor Attribution"]
        I5["CVE/Exploit Tracking"]
    end

    %% Fluxo Principal
    A --> B1
    A --> B2
    A --> B3
    A --> B4
    A --> B5

    B1 --> C1
    B2 --> D1
    B3 --> E1
    B4 --> F1
    B5 --> G1

    %% Conexões entre catálogos e busca
    C1 --> C2
    C2 --> C3
    C3 --> C4
    C4 --> C5
    C5 --> C6

    C6 --> D1
    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> D5
    D5 --> D6

    %% Análise de conteúdo
    D6 --> E1
    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 --> E5
    E5 --> E6

    %% Fóruns específicos
    E1 --> F1
    E1 --> F2
    E1 --> F3
    E1 --> F4
    E1 --> F5
    E1 --> F6

    %% Análise técnica
    F6 --> G1
    G1 --> G2
    G2 --> G3
    G3 --> G4
    G4 --> G5
    G5 --> G6

    %% Documentação
    G6 --> H1
    H1 --> H2
    H2 --> H3
    H3 --> H4
    H4 --> H5

    %% Threat Intelligence
    H5 --> I1
    I1 --> I2
    I2 --> I3
    I3 --> I4
    I4 --> I5

    %% Especialização por tipo
    E2 --> CHATS["Chats Anônimos"]
    CHATS --> CHAT1["BlackHat Chat"]
    CHATS --> CHAT2["WSS.chat"]
    CHATS --> CHAT3["Abyss"]

    E3 --> PASTE["Pastebins"]
    PASTE --> PASTE1["V3 Paste"]
    PASTE --> PASTE2["Stronghold"]

    E5 --> TI["🚨 Monitoramento TI"]
    TI --> TI1["Ransomware Groups"]
    TI --> TI2["Breach Forums"]
    TI --> TI3["Carding Forums"]
```

**📖 Guia de Uso do Fluxo Dark Web:**

1. **🛡️ OPSEC Crítico**: Configure ambiente ultra-seguro (Tails/Whonix + VPN)
2. **🎭 Sock Puppets**: Use personas fictícias criadas especificamente para investigação
3. **🔍 Busca Sistemática**: Percorra catálogos → motores → fóruns específicos
4. **📊 Categorização**: Organize achados por tipo (fóruns, chats, pastebins, etc.)
5. **🇺🇳 Análise Regional**: Explore fóruns regionais baseados no alvo
6. **🔧 Ferramentas Automatizadas**: Use OnionScan, TorBot para análise técnica
7. **📝 Documentação Segura**: Capture evidências censuradas e metadados
8. **🚨 Threat Intelligence**: Extraia IOCs, TTPs para análise de ameaças

**🚨 Alertas Críticos de Segurança:**
- ✅ **SEMPRE** use Tails ou Whonix para acesso
- ✅ **SEMPRE** configure VPN antes do Tor
- ✅ **NUNCA** baixe arquivos executáveis
- ✅ **NUNCA** use credenciais reais
- ✅ **SEMPRE** documente com timestamps e fontes
- ❌ **NUNCA** acesse sem autorização legal formal
- ❌ **NUNCA** participe em atividades ilícitas

**📚 Recursos Detalhados**:
- [Diretório Completo de Recursos Onion](diretorio-recursos-onion.md)
- [Guia OSINT Dark Web](../osint_darkweb_doc.md)
- [Checklist OPSEC](../../checklists/checklist-opsec.md)
```
