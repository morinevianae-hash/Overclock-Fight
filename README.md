# Configuração de IP Fixo no Windows 11 para Lan House

Tutorial rápido para configurar o endereço IP fixo dos computadores de uma lan house usando o painel clássico de conexões de rede do Windows 11.

## Estrutura da rede

| Equipamento | Endereço IP |
|---|---:|
| Roteador | `192.168.0.1` |
| Servidor | `192.168.0.2` |
| PC Cliente 01 | `192.168.0.3` |
| PC Cliente 02 | `192.168.0.4` |
| PC Cliente 03 | `192.168.0.5` |
| PC Cliente 04 | `192.168.0.6` |
| PC Cliente 05 | `192.168.0.7` |
| PC Cliente 06 | `192.168.0.8` |
| PC Cliente 07 | `192.168.0.9` |
| PC Cliente 08 | `192.168.0.10` |

Configuração comum para o servidor e todos os clientes:

```text
Máscara de sub-rede: 255.255.255.0
Gateway padrão:      192.168.0.1
DNS preferencial:    192.168.0.1
DNS alternativo:     deixar em branco
```

> [!IMPORTANT]
> Cada computador deve ter um endereço IP diferente. Nunca configure o mesmo IP em dois equipamentos.

## Passo a passo

### 1. Abrir as conexões de rede

1. Pressione `Windows + R`.
2. Digite o comando:

```text
ncpa.cpl
```

3. Pressione `Enter`.

### 2. Abrir as propriedades da rede

1. Localize a conexão utilizada pelo computador, normalmente chamada **Ethernet**.
2. Clique com o botão direito sobre **Ethernet**.
3. Clique em **Propriedades**.

### 3. Desativar o IPv6

1. Localize **Protocolo IP Versão 6 (TCP/IPv6)**.
2. Desmarque a caixa dessa opção.

> Nesta configuração da lan house, será utilizado o IPv4.

### 4. Abrir as propriedades do IPv4

1. Selecione **Protocolo IP Versão 4 (TCP/IPv4)**.
2. Clique em **Propriedades**.
3. Marque **Usar o seguinte endereço IP**.

### 5. Configurar o endereço IP

Digite o endereço reservado para o computador. Exemplo para o **PC Cliente 01**:

```text
Endereço IP:         192.168.0.3
Máscara de sub-rede: 255.255.255.0
Gateway padrão:      192.168.0.1
```

Nos demais computadores, altere somente o endereço IP conforme a tabela apresentada no início deste tutorial.

### 6. Configurar o DNS

Marque **Usar os seguintes endereços de servidor DNS** e preencha:

```text
Servidor DNS preferencial: 192.168.0.1
Servidor DNS alternativo:  deixar em branco
```

### 7. Salvar

1. Clique em **OK**.
2. Clique novamente em **OK** ou **Fechar**.
3. Repita o procedimento nos demais computadores, usando o IP correto para cada equipamento.

## Testar a configuração

Abra o **Prompt de Comando** e execute:

```bat
ipconfig
```

Teste a comunicação com o roteador:

```bat
ping 192.168.0.1
```

Teste a comunicação com o servidor:

```bat
ping 192.168.0.2
```

Se aparecer uma resposta parecida com esta, a comunicação está funcionando:

```text
Resposta de 192.168.0.1: bytes=32 tempo<1ms TTL=64
```

## Checklist

- [ ] Roteador configurado como `192.168.0.1`
- [ ] Servidor configurado como `192.168.0.2`
- [ ] Clientes configurados de `192.168.0.3` até `192.168.0.10`
- [ ] Máscara configurada como `255.255.255.0`
- [ ] Gateway configurado como `192.168.0.1`
- [ ] DNS preferencial configurado como `192.168.0.1`
- [ ] IPv6 desativado nos computadores desta rede
- [ ] Todos os computadores respondem ao roteador
- [ ] Todos os clientes conseguem se comunicar com o servidor

## Observações

- Faça a configuração utilizando uma conta com permissão de administrador.
- Confirme o IP de cada computador antes de salvar.
- Se a conexão parar de funcionar, verifique o cabo Ethernet, a máscara, o gateway e o DNS.
- Reserve os endereços de `192.168.0.2` até `192.168.0.10` no roteador ou mantenha-os fora da faixa DHCP para evitar conflitos.

---

Material criado para documentar a configuração da rede local de uma lan house com Windows 11.
