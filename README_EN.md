# Bunkr - A Password Manager Even Your Grandma Can Use

## What Are We Building?

A password manager that's **truly secure** and **ridiculously easy to use** — so easy that your 70-year-old grandmother can use it without calling you for help.

### Why Does This Matter?

**The problem:** Everyone uses "123456" or "dog_name2024" because password managers like 1Password and Bitwarden are too complicated for non-tech people. And when you try to teach a family member how to use one, they get lost.

**Our solution:** Build a password manager that is:
- As secure as the best out there (state-of-the-art encryption)
- So simple anyone can use it without a tutorial
- Free forever - no limits
- Possibly open source (like Bitwarden)

### The Differentiator

**Bitwarden/1Password are built for nerds.** We're building for regular people:

- Interface so clean it doesn't intimidate
- Onboarding that explains things in plain language (no tech jargon)
- Mobile keyboard that "just works"
- Browser extension that needs no manual

**Concrete example:**
- Bitwarden: "Configure your TOTP seed and enable 2FA via FIDO2"
- Bunkr: "Want to add an extra layer of security? Tap here 👆"

---

## What We're Building (MVP - Q2 2026)

### 1. **Native Mobile Apps**
- **iOS** (Swift + SwiftUI)
  - iOS keyboard integration
  - Face ID / Touch ID
  - Auto-fill in any app

- **Android** (Kotlin + Jetpack Compose)
  - Android keyboard integration
  - Biometrics
  - Native auto-fill

**Why native?** To get that fluid, reliable experience. Cross-platform (React Native/Flutter) doesn't deliver the same quality for keyboards and biometrics.

### 2. **Browser Extensions**
- Chrome, Firefox, Edge, Safari
- Auto-fill passwords
- Automatic login form detection
- Strong password generator
- Minimalist interface (small, straight-to-the-point popup)

### 3. **Web Dashboard**
- Interface to manage all your passwords
- Add/edit/delete logins
- Generate secure passwords
- See which devices you're logged in from
- SUPER clean design (think: Notion, not AWS admin panel)

### 4. **Secure Backend**
- NestJS + TypeScript
- PostgreSQL
- Cloudflare R2 (encrypted vault storage)
- Zero-knowledge architecture (even we can't see your passwords)

---

## Security (The Serious Part)

### Zero-Knowledge Architecture

```
Your master password → Derives encryption key → Encrypts vault locally → Uploads to server ALREADY ENCRYPTED
```

**Result:** Even if our servers get hacked, attackers only find useless encrypted blobs.

### Encryption
- AES-256-GCM (same standard banks use)
- Argon2id for key derivation (GPU-resistant)
- Each vault has its own key

---

## Why Join?

### 1. **Real Learning**
- Applied cryptography (you don't implement this every day)
- Native mobile development
- Zero-knowledge architecture
- Browser extensions

### 2. **Standout Portfolio**
- Not just another CRUD app
- Real security project
- Open source = visibility

### 3. **Real Impact**
- Helping people who actually need it
- Your parents/grandparents will be able to use it
- Contributing to a safer world

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| iOS | Swift + SwiftUI |
| Android | Kotlin + Jetpack Compose |
| Web | React + TypeScript |
| Backend | NestJS + TypeScript (maybe Rust for the Crypto core library) |
| Database | PostgreSQL (Supabase) |
| Storage | Supabase Storage |
| Infra | Terraform |
| CI/CD | GitHub Actions |

---

## Next Steps

1. Assemble the team (you're here!)
2. Define responsibilities
3. Initial monorepo setup with NX
4. MVP development
5. MVP launch - Q2 2026

---

If you like the idea, let's schedule a call to discuss!

🔐 **Bunkr** - Simple security for everyone.