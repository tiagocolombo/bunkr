# Bunkr - Um Gerenciador de Senhas que Até Sua Avó Consegue Usar

## O Que Estamos Construindo?

Um gerenciador de senhas **verdadeiramente seguro** e **ridiculamente fácil de usar** — tão fácil que sua avó de 70 anos consegue usar sem te ligar pedindo ajuda.

### Por Que Isso Importa?

**O problema:** Todo mundo usa "123456" ou "nome_do_cachorro2024" porque gerenciadores de senha como 1Password e Bitwarden são complicados demais para pessoas não-técnicas. E quando você tenta ensinar um familiar a usar, eles ficam perdidos.

**Nossa solução:** Construir um gerenciador de senhas que seja:
- Tão seguro quanto os melhores do mercado (criptografia de ponta)
- Tão simples que qualquer um consegue usar sem tutorial
- Gratuito para sempre - sem limites
- Possivelmente open source (como o Bitwarden)

### O Diferencial

**Bitwarden/1Password são feitos para nerds.** Estamos construindo para pessoas normais:

- Interface tão limpa que não intimida
- Onboarding que explica as coisas em linguagem simples (sem jargão técnico)
- Teclado mobile que "simplesmente funciona"
- Extensão de navegador que não precisa de manual

**Exemplo concreto:**
- Bitwarden: "Configure seu TOTP seed e habilite 2FA via FIDO2"
- Bunkr: "Quer adicionar uma camada extra de segurança? Toque aqui 👆"

---

## O Que Estamos Construindo (MVP - Q2 2026)

### 1. **Apps Mobile Nativos**
- **iOS** (Swift + SwiftUI)
  - Integração com teclado iOS
  - Face ID / Touch ID
  - Auto-preenchimento em qualquer app

- **Android** (Kotlin + Jetpack Compose)
  - Integração com teclado Android
  - Biometria
  - Auto-preenchimento nativo

**Por que nativo?** Para ter aquela experiência fluida e confiável. Cross-platform (React Native/Flutter) não entrega a mesma qualidade para teclados e biometria.

### 2. **Extensões de Navegador**
- Chrome, Firefox, Edge, Safari
- Auto-preenchimento de senhas
- Detecção automática de formulários de login
- Gerador de senhas fortes
- Interface minimalista (popup pequeno e direto ao ponto)

### 3. **Dashboard Web**
- Interface para gerenciar todas as suas senhas
- Adicionar/editar/deletar logins
- Gerar senhas seguras
- Ver de quais dispositivos você está logado
- Design SUPER limpo (pense: Notion, não painel admin da AWS)

### 4. **Backend Seguro**
- NestJS + TypeScript
- PostgreSQL
- Cloudflare R2 (armazenamento de cofre criptografado)
- Arquitetura zero-knowledge (nem nós conseguimos ver suas senhas)

---

## Segurança (A Parte Séria)

### Arquitetura Zero-Knowledge

```
Sua senha mestra → Deriva chave de criptografia → Criptografa cofre localmente → Envia para servidor JÁ CRIPTOGRAFADO
```

**Resultado:** Mesmo se nossos servidores forem hackeados, os atacantes só encontram blobs criptografados inúteis.

### Criptografia
- AES-256-GCM (mesmo padrão que bancos usam)
- Argon2id para derivação de chaves (resistente a GPU)
- Cada cofre tem sua própria chave

---

## Por Que Participar?

### 1. **Aprendizado Real**
- Criptografia aplicada (você não implementa isso todo dia)
- Desenvolvimento mobile nativo
- Arquitetura zero-knowledge
- Extensões de navegador

### 2. **Portfólio Diferenciado**
- Não é só mais um app CRUD
- Projeto de segurança real
- Open source = visibilidade

### 3. **Impacto Real**
- Ajudar pessoas que realmente precisam
- Seus pais/avós vão conseguir usar
- Contribuir para um mundo mais seguro

---

## Stack Tecnológica

| Componente | Tecnologia |
|-----------|--------------|
| iOS | Swift + SwiftUI |
| Android | Kotlin + Jetpack Compose |
| Web | React + TypeScript |
| Backend | NestJS + TypeScript (talvez Rust para a biblioteca core de Crypto) |
| Banco de Dados | PostgreSQL (Supabase) |
| Armazenamento | Supabase Storage |
| Infra | Terraform |
| CI/CD | GitHub Actions |

---

## Próximos Passos

1. Montar o time (você está aqui!)
2. Definir responsabilidades
3. Setup inicial do monorepo com NX
4. Desenvolvimento do MVP
5. Lançamento do MVP - Q2 2026

---

Se você curtiu a ideia, vamos agendar uma call para discutir!

🔐 **Bunkr** - Segurança simples para todos.
