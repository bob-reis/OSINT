# OSINT Workflows (repo privado)

Guia visual de fluxos OSINT para **Domínio, E-mail, Localização, Nome Real, Telefone e Username**.  
Cada diagrama foi otimizado para leitura no GitHub (vertical e compacto).

## Índice
- [Fluxo: Domain Name](#fluxo-domain-name)
- [Fluxo: Email Address](#fluxo-email-address)
- [Fluxo: Location](#fluxo-location)
- [Fluxo: Real Name](#fluxo-real-name)
- [Fluxo: Telephone](#fluxo-telephone)
- [Fluxo: Username](#fluxo-username)

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
```

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
```
