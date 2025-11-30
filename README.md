# Ataques de Força Bruta com Medusa em Ambiente Controlado  
### *Projeto de Cibersegurança — DIO*

Este projeto apresenta testes práticos de força bruta utilizando Kali Linux e a ferramenta Medusa contra serviços vulneráveis hospedados em uma máquina Metasploitable 2 e na aplicação DVWA.  
O objetivo é compreender o funcionamento desses ataques, identificar vulnerabilidades e demonstrar técnicas de mitigação, tudo documentado de forma profissional.

---

# Sumário
- Objetivos do Projeto  
- Topologia do Ambiente  
- Configuração das Máquinas Virtuais  
- Ferramentas Utilizadas  
- Ataque de Força Bruta em FTP  
- Força Bruta em Formulário Web (DVWA)  
- Password Spraying em SMB  
- Mitigações Recomendadas  
- Arquivos do Repositório  
- Conclusões e Aprendizados  

---

# Objetivos do Projeto

Este projeto demonstra:

✔ Ataques de força bruta em diferentes serviços (FTP, Web e SMB)  
✔ Uso do Kali Linux como ambiente ofensivo  
✔ Domínio básico da ferramenta Medusa  
✔ Enumeração de serviços e usuários  
✔ Criação de wordlists simples  
✔ Montagem de relatório técnico estruturado  
✔ Identificação e mitigação de vulnerabilidades  

---

# Topologia do Ambiente

Rede: Host-Only / Interna (isolada)

DVWA: hospedado no mesmo ambiente vulnerável ou em VM separada.

---

# ⚙️ Configuração das Máquinas Virtuais

## Kali Linux
- Sistema atacante  
- Ferramentas pré-instaladas: Medusa, Nmap, Enum4Linux  
- Ajustes de rede: Host-Only no VirtualBox  

## Metasploitable 2
- Máquina vulnerável intencionalmente  
- Serviços utilizados para este projeto:
  - FTP
  - SMB (Samba)
  - Apache + DVWA

---

# Ferramentas Utilizadas

| Ferramenta | Finalidade |
|-----------|------------|
| Medusa | Testes de força bruta em serviços |
| Nmap | Descoberta de portas e versões |
| Enum4linux | Enumeração de usuários SMB |
| DVWA | Testes de força bruta em formulários web |
| Wordlists simples | Senhas para ataques |

---

# Ataque de Força Bruta em FTP

## Descobrindo serviço com Nmap
```bash
nmap -sV 192.168.56.101

