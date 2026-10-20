# ProtoProbe

## O que é

O ProtoProbe é uma ferramenta de Windows para diagnóstico de Modbus (TCP, RTU e ASCII), feita para técnicos e engenheiros de automação em campo ou na bancada.

- **Cliente:** conecta a um equipamento, lê as tags numa tabela que se edita como planilha e escreve valores.
- **Servidor:** o ProtoProbe se passa por um equipamento, para testar o seu sistema sem o equipamento real.
- **Quadros:** mostra os bytes que passaram no fio.

## Onde baixar

A versão mais recente está em https://github.com/Movi-Tech/ProtoProbe-release/releases/latest

Baixe o instalador (`ProtoProbe-v<versão>-setup.exe`) e o arquivo `.sha256` que vem junto dele.

## Como instalar

1. Baixe o instalador e o arquivo `.sha256` na página acima.
2. Confira o SHA-256 do instalador (veja o aviso abaixo).
3. Execute o instalador.
4. Escolha como instalar: a instalação é por usuário, sem precisar de administrador, e há a opção de instalar para todos os usuários do computador.
5. Leia e aceite os [Termos de Uso](TERMOS-DE-USO.md) quando o instalador e o programa pedirem.
6. Abra o ProtoProbe pelo menu Iniciar.

Requisito: Windows 10 ou 11, 64 bits.

### Portátil

A partir da 0.15, a página de versões traz também `ProtoProbe-v<versão>-portable.zip`, com o seu `.sha256`, para usar o programa sem instalar:

1. Baixe o `.zip` e confira o SHA-256.
2. Extraia tudo para uma pasta, de preferência perto da raiz do disco ou num pen drive.
3. Abra o `ProtoProbe.exe` e aceite os [Termos de Uso](TERMOS-DE-USO.md).

As preferências ficam em `ProtoProbe.ini` e o espaço de trabalho e a biblioteca de equipamentos, na pasta `dados`, ao lado do programa. Para atualizar, extraia o zip novo por cima da pasta. Para apagar tudo, apague a pasta.

## Aviso do SmartScreen

Hoje o instalador não tem certificado de assinatura de código. Por isso, na primeira execução, o Windows mostra o aviso "O Windows protegeu seu computador". Para continuar:

1. Clique em **Mais informações**.
2. Clique em **Executar assim mesmo**.

Antes de executar, recomendamos conferir o SHA-256 do instalador. No PowerShell, na pasta do download:

```
Get-FileHash .\ProtoProbe-v<versão>-setup.exe -Algorithm SHA256
```

O valor deve ser igual ao que está no arquivo `.sha256` baixado junto. Se for diferente, não execute o instalador.

## Próximas versões

Esta lista mostra a direção do ProtoProbe, versão por versão. Sem compromisso de prazo: a ordem e o conteúdo podem mudar.

### 0.14.0

Uma linha nova no fim da tabela, para digitar ou colar tags; tempo limite e tentativas ajustáveis em cada aba; aceite dos Termos de Uso; menu Ajuda com a tela Sobre. Toda versão nova passa primeiro por um teste público ("Em Teste") antes de chegar a quem usa. A versão mais nova está sempre na página de releases.

### 0.15

- árvore do projeto: equipamentos, variáveis, gráficos e pastas numa árvore ao lado, como no TIA Portal;
- biblioteca de equipamentos: salve as tags e a conexão de um modelo e reaproveite depois, informando só o endereço;
- modo portátil: o programa roda sem instalar, de uma pasta ou de um pen drive, e sugere a instalação;
- simulação no Servidor: cada variável pode variar sozinha (aleatória, rampa, senoide e outros tipos) para imitar um equipamento real;
- vários servidores TCP ao mesmo tempo, cada um na sua porta ou endereço;
- Localizar Equipamentos melhor: um ID que não responde não interrompe a busca, há escolha do método de busca (leitura, FC43 ou FC17) e a tabela mostra só quem respondeu;
- faixas de endereço: Ping com IP de início e de fim, Telnet com porta de início e de fim, e Localizar Equipamentos com as duas faixas.

### Depois da 0.15

Atualizações assinadas: o programa só aceita atualização publicada pela Movi Automação.

### Depois

- OPC UA
- Siemens S7
- EtherNet/IP

## Termos de Uso

- [Termos de Uso](TERMOS-DE-USO.md)
