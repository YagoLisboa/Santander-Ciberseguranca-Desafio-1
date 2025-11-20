# Relatório Acadêmico – Auditoria de Segurança com Kali Linux, Medusa e Ambientes Vulneráveis

## **1. Introdução**
Este relatório apresenta a análise, execução e documentação de um laboratório prático de auditoria de segurança realizado em ambiente controlado, utilizando as ferramentas **Kali Linux**, **Medusa**, **Metasploitable 2** e **DVWA (Damn Vulnerable Web Application)**. O objetivo principal foi compreender, na prática, como ocorrem ataques de força bruta, automação de tentativas de autenticação e password spraying, bem como propor medidas de mitigação eficazes.

A atividade foi desenvolvida com foco educacional, de forma ética e sem riscos a sistemas reais.

---

## **2. Objetivos do Projeto**
- Explorar ataques de autenticação em diferentes serviços (FTP, Web e SMB).
- Utilizar o Medusa como ferramenta de auditoria e testes controlados.
- Documentar a configuração do ambiente, comandos, conceitos e reflexões.
- Analisar vulnerabilidades e sugerir boas práticas de mitigação.
- Desenvolver documentação profissional para portfólio acadêmico.

---

## **3. Configuração do Ambiente**

### **3.1 Ferramentas Utilizadas**
- **Kali Linux**: máquina atacante com ferramentas de análise e auditoria.
- **Metasploitable 2**: ambiente vulnerável para simulações.
- **DVWA**: aplicação web intencionalmente vulnerável para estudo.
- **VirtualBox**: virtualização com rede Host-Only.

### **3.2 Topologia do Laboratório**
- As máquinas foram configuradas em rede isolada (host-only), garantindo isolamento total da internet.
- Foram definidos IPs estáticos para facilitar testes.

### **3.3 Identificação de Serviços**
A identificação inicial de serviços foi feita via análise de portas e banners. A visualização dos serviços disponíveis foi essencial para direcionar os cenários de teste.

---

## **4. Cenário 1 – Estudo de Força Bruta em FTP**

### **4.1 Contexto**
O FTP é um protocolo antigo que transmite credenciais em texto puro. Isso o torna vulnerável em ambientes sem criptografia ou políticas de segurança apropriadas.

### **4.2 Objetivo do Teste**
Simular tentativas de força bruta utilizando uma wordlist personalizada, demonstrando riscos associados a senhas fracas.

### **4.3 Procedimento (Descrição Conceitual)**
- Identificação do serviço ativo.
- Geração de uma wordlist simples.
- Utilização do Medusa para realizar tentativas controladas de autenticação.

### **4.4 Reflexões e Resultados**
O teste demonstrou como senhas previsíveis podem ser comprometidas rapidamente e reforçou a importância de políticas de senhas fortes e autenticação segura.

### **4.5 Medidas de Mitigação**
- Substituição do FTP por SFTP.
- Implementação de bloqueios progressivos.
- Políticas de senha forte.
- Registro de tentativas e análise contínua.

---

## **5. Cenário 2 – Automação de Tentativas em Formulário Web (DVWA)**

### **5.1 Contexto**
Formulários web vulneráveis permitem exploração por força bruta ou automação de tentativas, especialmente em aplicações sem CAPTCHA ou limites de tentativas.

### **5.2 Objetivo do Teste**
Avaliar o comportamento do DVWA ao receber múltiplas tentativas consecutivas de login.

### **5.3 Procedimento (Descrição Conceitual)**
- Análise do método POST utilizado pelo formulário.
- Estudo da resposta da aplicação a tentativas repetidas.
- Automação controlada das tentativas para fins de auditoria.

### **5.4 Reflexões e Resultados**
O DVWA demonstrou ausência de proteções modernas, como CAPTCHA ou 2FA, evidenciando vulnerabilidades comuns em aplicações mal configuradas.

### **5.5 Medidas de Mitigação**
- Implementação de CAPTCHA.
- Rate limiting.
- Autenticação multifator.
- Validação adequada no backend.

---

## **6. Cenário 3 – Password Spraying em SMB com Enumeração de Usuários**

### **6.1 Contexto**
O password spraying é uma técnica de tentativa de autenticação que utiliza uma única senha contra múltiplos usuários, reduzindo risco de bloqueio.

### **6.2 Objetivo do Teste**
Avaliar como o serviço SMB da Metasploitable responde a tentativas controladas com contas enumeradas.

### **6.3 Procedimento (Descrição Conceitual)**
- Enumeração de possíveis nomes de usuário.
- Simulação de tentativas de autenticação com senha padrão.

### **6.4 Reflexões e Resultados**
O teste demonstrou riscos elevados quando contas utilizam senhas fracas ou padronizadas, especialmente em serviços como SMB, amplamente usado em redes corporativas.

### **6.5 Medidas de Mitigação**
- Desabilitar contas não utilizadas.
- Políticas de senhas fortes e únicas.
- Auditoria e registro de tentativas.
- Atualização e endurecimento do serviço SMB.

---

## **7. Discussão Geral e Conclusões**
A execução deste projeto possibilitou compreender, em ambiente seguro, como ataques contra mecanismos de autenticação são estruturados e por que medidas preventivas são fundamentais.

O estudo reforça a importância de:
- Manutenção contínua de sistemas.
- Monitoramento de logs.
- Políticas de senha robustas.
- Uso de ferramentas adequadas de auditoria.
- Desenvolvimento seguro de aplicações.

O laboratório demonstrou que vulnerabilidades simples podem ser exploradas rapidamente caso medidas de mitigação não sejam aplicadas.

---

## **8. Referências Bibliográficas**
*(Adicione suas referências acadêmicas aqui conforme normas da instituição.)*

