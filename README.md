# Netrunner Studio — Alpha A_0.4.7

O Netrunner Studio é um estúdio de produção ao vivo para Windows, com
canvas horizontal 16:9 e vertical 9:16, Prévia/Programa, cenas, fontes,
mixer de áudio, transições e controles em um fluxo inspirado no OBS, com
identidade própria.

Este repositório é o canal público de distribuição para testers. O código
próprio do Netrunner Studio permanece fechado no repositório privado de
desenvolvimento; esta página e as Releases publicam somente os artefatos de
instalação e verificação, nunca os arquivos-fonte próprios.

## Download e instalação

Baixe a [Release A_0.4.7](https://github.com/Rk7gamerYT/netrunner-studio-alpha/releases/tag/v0.4.7)
e siga estes passos:

1. Baixe `NetrunnerStudio-A_0.4.7-Installer-Windows-x64.zip`.
2. Extraia o ZIP para uma pasta local.
3. Execute `NetrunnerStudio-Alpha-Setup-0.4.7.exe`.
4. Abra o Netrunner Studio pelo atalho criado no Menu Iniciar ou na área de
   trabalho.

O instalador é por usuário e não precisa de privilégios de administrador.
Nesta variante alpha bundled, Python e uma instalação separada do OBS Studio
não são necessários para executar o app.

## Verificação do download

O ZIP inclui o arquivo `NetrunnerStudio-A_0.4.7-Installer.sha256`. Depois de
extrair o instalador, no PowerShell execute:

```powershell
Get-FileHash .\NetrunnerStudio-Alpha-Setup-0.4.7.exe -Algorithm SHA256
```

Compare o resultado com o hash publicado no arquivo `.sha256`. O instalador
não possui assinatura Authenticode reconhecida nesta fase; o Windows pode
exibir um aviso do SmartScreen mesmo quando o hash está correto.

## Destaques da A_0.4.7

- Modo Estúdio com Prévia e Programa independentes.
- Canvas horizontal e vertical sincronizados quando o destino conjunto está
  habilitado.
- Publicação com ciclo real de transição, incluindo Corte, Fade, Swipe e
  Slide, com bloqueio do botão até a conclusão.
- Cenas e fontes com salvamento automático após alterações confirmadas.
- `Ctrl+Z` para desfazer alterações estruturais e transformações do canvas.
- Mixer de áudio, controles de transmissão/gravação e composição isolada na
  Prévia.
- Runtime necessário do OBS Studio bundled nesta build alpha, com os avisos e
  licenças correspondentes dentro da instalação.
- Correção do crash de fechamento durante transições do Modo Estúdio.
- Persistência de projeto e rascunho da Prévia validada após reinicialização.
- Cobertura permanente para WebSocket, efeitos, animações, gravação,
  Multi-RTMP e Cenas Vinculadas.
- Revisões pontuais de performance no motor nativo e na interface.
- Menu de contexto de fontes organizado por categorias, com comandos de
  composição, transformação, pré-visualização e atalhos inspirados no OBS.
- Diálogos de propriedades de transição redesenhados, com prévia A/B compacta,
  campos alinhados e seletor de cor mais claro.

## Avisos da versão alpha

Esta é uma versão de testes. Podem existir bugs, incompatibilidades com
hardware específico ou avisos do antivírus/SmartScreen. Para reportar um
problema, informe a versão do Windows, GPU, passo a passo para reproduzir,
transição/canvas usados e, se possível, o horário do teste e uma captura.

Não substitua os arquivos instalados manualmente. Para testar uma versão nova,
instale o pacote correspondente pela Release; o instalador mantém a
instalação por usuário em `%LOCALAPPDATA%\Netrunner Studio`.

## Licenças

O código próprio, a marca e os recursos do Netrunner Studio não são publicados
neste repositório. A build bundled inclui componentes do OBS Studio sob GPLv2,
com a licença, os avisos de terceiros e a referência ao código-fonte
correspondente dentro da instalação.
