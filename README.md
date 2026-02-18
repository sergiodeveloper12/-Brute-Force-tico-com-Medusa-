# -Brute-Force-tico-com-Medusa-

# Auditoria de Segurança: Ataques de Força Bruta com Medusa no Kali Linux

Este repositório documenta um laboratório prático realizado como parte do curso de Cybersecurity da DIO. O objetivo foi simular ataques de força bruta e password spraying em ambiente controlado e isolado, utilizando a ferramenta **Medusa** no Kali Linux, contra serviços vulneráveis no **Metasploitable 2** e no **DVWA** (Damn Vulnerable Web Application).

**Aviso importante**: Todas as atividades foram realizadas exclusivamente em ambiente de laboratório virtualizado (VirtualBox, rede Host-Only), sem qualquer impacto em sistemas reais. Este projeto tem fins exclusivamente educacionais e de auditoria ética.

## Objetivos do Laboratório

- Configurar um ambiente seguro para testes de penetração
- Executar ataques de força bruta em serviços FTP, HTTP (formulário web) e SMB
- Utilizar a ferramenta Medusa para testes paralelos e modulares
- Documentar comandos, resultados e evidências
- Identificar vulnerabilidades exploradas e propor medidas de mitigação

## Ambiente Configurado

- **Máquina Atacante**: Kali Linux (versão mais recente, atualizada)
- **Máquina Alvo**: Metasploitable 2 (IP exemplo: 192.168.56.101)
- **Aplicação Web Vulnerável**: DVWA (instalado no Metasploitable 2, nível de segurança Low)
- **Rede**: Host-Only Adapter no VirtualBox (isolada da internet e da rede física)
- **Ferramentas principais**: Medusa, Nmap (para enumeração inicial), wordlists personalizadas e rockyou.txt

## Metodologia e Testes Realizados

### 1. Enumeração Inicial
```bash
nmap -sV -p- 192.168.56.101
