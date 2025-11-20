# Santander-Ciberseguranca-Desafio-1
Neste desafio utilizo um Kali Linux Bootável e faço um experimento de quebra de senhas com o Medusa.

# Auditoria de Segurança com Kali Linux, Medusa e Ambientes Vulneráveis

Este repositório contém a documentação do projeto de auditoria de segurança utilizando **Kali Linux**, **Medusa**, **Metasploitable 2** e **DVWA**, conduzido em um ambiente controlado para fins acadêmicos.

## 📌 Objetivos do Projeto
- Compreender ataques de força bruta em serviços como FTP, SMB e formulários Web.
- Utilizar o Medusa para auditoria de autenticação.
- Documentar processos, reflexões, comandos e boas práticas.
- Propor medidas de mitigação a vulnerabilidades identificadas.
- Publicar documentação técnica como portfólio no GitHub.

---

## 🧪 Ambiente Utilizado
- **Kali Linux** (máquina atacante)
- **Metasploitable 2** (máquina alvo)
- **DVWA** instalado no ambiente alvo
- **VirtualBox** com rede Host-Only

---

## 🔍 Cenários de Teste
### 1. Força Bruta em FTP
- Identificação do serviço
- Wordlist personalizada
- Tentativas de autenticação com Medusa
- Reflexões sobre risco e mitigação

### 2. Automação de Tentativas em DVWA
- Análise do funcionamento do formulário
- Automação de tentativas (HTTP)
- Impacto da ausência de controles (CAPTCHA, rate limiting)

### 3. Password Spraying em SMB
- Enumeração de usuários
- Tentativas controladas de autenticação com uma senha comum

---

## 📁 Estrutura do Repositório
```
|-- README.md
|-- Files/
  |-- Relatorio-Técnico.pdf (gerado separadamente)
  |-- RELATORIO-ACADEMICO.md
```

---

## 🛡️ Boas Práticas & Mitigações
- Uso de MFA
- Políticas de senhas fortes
- Rate limiting e captura de tentativas
- Remoção de serviços desnecessários
- Substituição de protocolos inseguros

---

## 🧾 Licença
Este projeto é apenas para fins educacionais. Não utilize técnicas apresentadas aqui em sistemas reais sem autorização formal.

---

## 📚 Autor
**Yago Lisboa**

Projeto desenvolvido como parte da disciplina de Cibersegurança.
