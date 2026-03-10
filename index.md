---
layout: post
title: "O que é Shift‑Left Security"
date: 2026-03-10
categories: [Security, DevSecOps]
tags: [Shift-Left, GitHub Advanced Security, GHAS, CodeQL]
---

## O que é Shift‑Left Security

O **Shift‑Left Security** coloca a segurança de software no centro do desenvolvimento. Em vez de tratar a segurança como um item de verificação final ao término do **SDLC**, essa abordagem incorpora práticas de segurança desde o primeiro dia.

Ao identificar vulnerabilidades precocemente, as equipes reduzem o tempo, o custo e o esforço necessários para correções, entregando softwares muito mais seguros e confiáveis.

---

## Shift‑Left Security: Um Novo Paradigma

O Shift‑Left Security representa uma mudança fundamental na forma como as organizações encaram a segurança de aplicações.

Ao trazer as preocupações de segurança para as fases iniciais do desenvolvimento, as equipes conseguem identificar e tratar vulnerabilidades de forma **proativa**, antes que se tornem problemas críticos em produção.

---

## Integração da Segurança desde o Início

O Shift‑Left Security começa com a incorporação dos **requisitos de segurança já na fase de design**.

Dessa forma, a segurança passa a ser um componente central da arquitetura do sistema desde a concepção do projeto — e não apenas um ajuste posterior. O resultado é uma **entrega de software mais rápida, segura e competitiva**.

---

## Segurança Contínua além de SAST/DAST com GitHub Advanced Security (GHAS)

O **GitHub Advanced Security (GHAS)** fortalece os testes automatizados ao longo de todo o **SDLC**, oferecendo controles adicionais que ampliam a estratégia de Shift‑Left.

---

### 🔐 Secret Scanning + Push Protection

- Detecta vazamento de credenciais como **API keys, tokens e senhas**
- **Bloqueia automaticamente o push** quando um segredo é identificado
- Analisa todo o histórico do repositório


![Code scanning](/assets/images/shift-left/code-scanning.png)





![Code scanning](/assets/images/shift-left/code-scanning-02.png)


---

### 📦 Software Composition Analysis (SCA)

#### Dependabot + Dependency Review

- Identifica bibliotecas vulneráveis **antes do merge**
- Abre **pull requests automáticos** com correções
- Avalia riscos de novas dependências adicionadas ao código


![Code scanning](/assets/images/shift-left/sca.png)

![Code scanning](/assets/images/shift-left/sca-02.png)


---

### 🧪 Code Scanning (CodeQL)

O **Code Scanning** analisa o código fonte **antes do merge e antes do deploy**.

Executa análises em:
- Pull Requests  
- Commits  
- Pipelines de CI (GitHub Actions)

Isso permite detectar vulnerabilidades quando os desenvolvedores **ainda estão codando**.


![Code scanning](/assets/images/shift-left/secret-scanning.png)

![Code scanning](/assets/images/shift-left/secret-scanning-02.png)


---

## GitHub Autofix

O **GitHub Autofix** funciona **sobre o GHAS Code Scanning (CodeQL)**:

1. Uma vulnerabilidade é detectada durante o desenvolvimento
2. O Autofix gera uma **correção contextualizada**
3. A correção é sugerida **antes do merge**, muitas vezes como uma sugestão de PR

Isso leva a **remediação para a esquerda**, e não apenas a detecção.

---

## Como Ativar o GitHub Advanced Security

Essa opção ativa automaticamente:

- CodeQL  
- Secret Scanning  
- Dependabot  
- Push Protection  

### Caminho de Configuração

Essa opção ativa automaticamente CodeQL, Secret Scanning, Dependabot e Push Protection em massa.
Caminho:
-	Org → Settings
-	Security → Advanced Security → Configurations
-	Selecione GitHub recommended
-	Aplicar em: 
-	Todos os repositórios
ou
-	 Apenas novos repositórios



``
