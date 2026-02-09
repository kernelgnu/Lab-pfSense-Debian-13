# Etapa 4 – Configuração da Unidade Certificadora (CA) e Certificado HTTPS no pfSense

## Objetivo
Configurar uma Unidade Certificadora (CA) interna no pfSense e aplicar um certificado digital próprio para proteger o acesso à interface web via HTTPS, garantindo confidencialidade, integridade e autenticidade na administração do firewall.

---

## Ambiente
- **Firewall:** pfSense
- **Acesso:** Interface Web (GUI)
- **Contexto:** Laboratório virtualizado

---

## Procedimento Realizado
**Data:** 08/02/2026

### 1. Criação da Unidade Certificadora (CA)
O processo iniciou-se pela criação de uma CA interna no pfSense:

Caminho acessado:
- `System > Certificates > Authorities`

Ações executadas:
- Criação de uma **nova Certificate Authority** interna
- Definição dos parâmetros básicos da CA (nome, validade e algoritmo padrão)
- Salvamento da CA no repositório interno do pfSense
- **Exportação da CA**, permitindo sua instalação em máquinas clientes para evitar alertas de certificado não confiável

Essa CA passa a ser a entidade confiável responsável pela emissão de certificados internos do ambiente.

---

### 2. Criação e Aplicação do Certificado HTTPS
Após a criação da CA, foi configurado o certificado HTTPS utilizado pela interface administrativa do pfSense.

Ações realizadas:
- Geração de um **certificado digital assinado pela CA interna**
- Associação do certificado à interface web do pfSense
- Configuração do firewall para **utilizar HTTPS com o certificado criado**, substituindo o certificado padrão

Com isso, o acesso à GUI do pfSense passa a ser protegido por um certificado próprio e controlado pelo administrador do ambiente.

---

## Validação
- Acesso à interface web do pfSense realizado exclusivamente via **HTTPS**
- Certificado apresentado corresponde à CA criada
- Comunicação criptografada entre navegador e firewall

---

## Considerações de Segurança
- O uso de uma **CA interna** elimina dependência de certificados genéricos ou autoassinados sem controle.
- A exportação da CA permite estabelecer uma cadeia de confiança nos hosts internos.
- HTTPS é obrigatório em ambientes administrativos, mesmo em laboratório, para manter boas práticas operacionais.

---

## Observações
- Este processo serve como base para futuras configurações de **VPN (OpenVPN/IPsec)** e autenticação baseada em certificados.
- Em ambientes produtivos, recomenda-se controle rigoroso de validade e revogação de certificados.

