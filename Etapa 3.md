## Etapa 3 – Configuração de Acesso Seguro via SSH
**Data:** 08/02/2026

### 3.1 Ativação do Secure Shell (SSH)
Foi realizada a configuração de acesso remoto seguro ao pfSense utilizando SSH, com foco em administração controlada e rastreável.

Configurações aplicadas:
- Ativação do **Secure Shell (SSH)** no pfSense
- Habilitação do **Serial Terminal**, permitindo acesso administrativo alternativo em cenários de falha
- Ativação da **proteção do console por senha**, prevenindo acesso não autorizado local

Essas medidas garantem acesso administrativo seguro e reduzem o risco de comprometimento por acesso físico ou remoto não autorizado.

### 3.2 Integração do SSH com o Sistema de Logs
Para aumentar a visibilidade e a capacidade de auditoria, o serviço **sshd** foi adicionado ao sistema de logs do pfSense.

Benefícios dessa configuração:
- Registro de tentativas de login bem-sucedidas e falhas
- Facilidade na detecção de tentativas de força bruta
- Base para correlação futura com SIEM ou análise forense

### 3.3 Considerações de Segurança
- O uso de SSH centraliza a administração de forma segura e auditável.
- A proteção do console adiciona uma camada extra contra acessos físicos indevidos.
- O registro detalhado de eventos SSH é essencial para ambientes monitorados e práticas de Blue Team.