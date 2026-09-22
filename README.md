# Netrunner Studio — Beta B_0.5.4

O Netrunner Studio é um estúdio de produção ao vivo para Windows, com
canvas horizontal 16:9 e vertical 9:16, Prévia/Programa, cenas, fontes,
mixer de áudio, transições e controles em um fluxo inspirado no OBS, com
identidade própria.

Este repositório é o canal público de distribuição para testers. O código
próprio do Netrunner Studio permanece fechado no repositório privado de
desenvolvimento; esta página e as Releases publicam somente os artefatos de
instalação e verificação, nunca os arquivos-fonte próprios.

## Download e instalação

Baixe a [Release B_0.5.4](https://github.com/Rk7gamerYT/netrunner-studio-alpha/releases/tag/v0.5.4)
e siga estes passos:

1. Baixe `NetrunnerStudio-B_0.5.4-Installer-Windows-x64.zip`.
2. Extraia o ZIP para uma pasta local.
3. Execute `NetrunnerStudio-Beta-Setup-0.5.4.exe`.
4. Abra o Netrunner Studio pelo atalho criado no Menu Iniciar ou na área de
   trabalho.

O instalador é por usuário e não precisa de privilégios de administrador.
Nesta variante beta bundled, Python e uma instalação separada do OBS Studio
não são necessários para executar o app.

## Verificação do download

O ZIP inclui o arquivo `NetrunnerStudio-B_0.5.4-Installer.sha256`. Depois de
extrair o instalador, no PowerShell execute:

```powershell
Get-FileHash .\NetrunnerStudio-Beta-Setup-0.5.4.exe -Algorithm SHA256
```

Compare o resultado com o hash publicado no arquivo `.sha256`. O instalador
não possui assinatura Authenticode reconhecida nesta fase; o Windows pode
exibir um aviso do SmartScreen mesmo quando o hash está correto.

## Destaques da B_0.5.4

- Adicionado: suporte a AMD FidelityFX Super Resolution (FSR) para melhorar
  a nitidez de fontes redimensionadas -- filtros "Redimensionar FSR" e
  "Nitidez FSR" (Filtros → Adicionar).
- Adicionado: a opção "FSR" em Configurações → Vídeo → "Filtro de redução"
  (ambos os canvases) e no filtro de escala por item de cena.

## Destaques acumulados desde a B_0.5.0

- Corrigido (segurança): a senha do WebSocket ficava descriptografada na
  memória durante toda a sessão da tela de Configurações, mesmo sem clicar em
  "Mostrar".
- Corrigido: o Modo Estúdio não sincronizava com a Prévia uma fonte
  adicionada/removida numa cena já enviada ao vivo antes.
- Adicionado: arrastar cenas com o mouse para reorganizá-las.
- Corrigido: "Cenas Vinculadas" não funcionava corretamente durante o Modo
  Estúdio.
- Corrigido: "Cenas Vinculadas" não sobrevivia a um reinício do app.
- Ícone próprio na barra de tarefas enquanto grava ou transmite, no lugar do
  antigo selo roxo por cima do ícone normal.
- Suporte a gravação em MP4, MOV, FLV e MPEG-TS (além de MKV) e a codecs de
  áudio Opus, FLAC e PCM (além de AAC), com aviso explícito de que MP4/MOV
  não são tão resistentes a uma queda do app quanto o MKV.
- Pausar e retomar a gravação sem finalizar o arquivo, sem afetar uma
  transmissão simultânea do mesmo canvas.
- Faixas de áudio da gravação movidas para Configurações → Áudio.
- Correções de bugs reais reportados por usuários: exibição de dispositivo de
  áudio em Configurações, persistência das opções avançadas do Modo Estúdio e
  perda de filtros de áudio ao reselecionar um dispositivo.

- Modo Estúdio com Prévia e Programa independentes.
- Canvas horizontal e vertical sincronizados quando o destino conjunto está
  habilitado.
- Publicação com ciclo real de transição, incluindo Corte, Fade, Swipe e
  Slide, com bloqueio do botão até a conclusão.
- Cenas e fontes com salvamento automático após alterações confirmadas.
- `Ctrl+Z` para desfazer alterações estruturais e transformações do canvas.
- Mixer de áudio, controles de transmissão/gravação e composição isolada na
  Prévia.
- Runtime necessário do OBS Studio bundled nesta build beta, com os avisos e
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
- Destinos de transmissão configuráveis separadamente por canvas, incluindo
  o canvas Vertical.
- Renomeação de cenas e fontes com `F2` ou pelo menu do botão direito.
- Indicador roxo no ícone do app durante gravação ou transmissão ao vivo.
- Canais mutados do mixer apresentados em escala de cinza para distinção rápida.
- Correções de persistência e de consistência visual nos painéis de transmissão.
- Ícones SVG padronizados e cards de destinos com gradiente compartilhado,
  alinhamento consistente e suporte ao Kick, Trovo, Facebook e X.
- Captura de monitor usando DXGI por padrão, com restauração validada após
  reinício enquanto a captura estava ativa.

## Avisos da versão beta

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
