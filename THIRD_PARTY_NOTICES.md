# Netrunner Studio — avisos de terceiros

Este arquivo separa o código proprietário do Netrunner Studio das bibliotecas
usadas pelo produto. Os textos de licença incluídos no instalador são válidos
somente para os componentes correspondentes.

## OBS Studio / libobs 32.2.2

- Licença: GNU GPL v2.
- Projeto: <https://github.com/obsproject/obs-studio>
- Release usado no runtime: <https://github.com/obsproject/obs-studio/releases/tag/32.2.2>
- O texto da GPLv2 deve acompanhar qualquer pacote que inclua o runtime do
  OBS. O instalador bundled também deve oferecer acesso ao código-fonte
  correspondente do OBS, conforme a GPL.

## PySide6 / Qt for Python

- `PySide6`, `PySide6_Essentials`, `PySide6_Addons` e `shiboken6`: LGPL-3.0-only
  OR GPL-2.0-only OR GPL-3.0-only, conforme a opção escolhida na distribuição.
- O Netrunner usa a opção LGPL do PySide6; o código próprio continua separado e
  não é incorporado estaticamente ao Qt.
- Projeto: <https://wiki.qt.io/Qt_for_Python>
- Licença: <https://www.gnu.org/licenses/lgpl-3.0.html>

A camada Qt foi migrada de PyQt6 para PySide6 para evitar a dependência de uma
licença comercial. A distribuição ainda deve acompanhar este aviso e respeitar
as obrigações da LGPL, incluindo preservar os textos de licença e não impedir
que o usuário substitua as bibliotecas LGPL por versões compatíveis.

## psutil

- Licença: BSD-3-Clause.
- Projeto: <https://github.com/giampaolo/psutil>

## PyInstaller

- O bootloader é GPLv2 com a exceção específica que permite empacotar e
  distribuir programas não livres. Ele é ferramenta/infraestrutura de build,
  não código proprietário do Netrunner Studio.
- Projeto: <https://github.com/pyinstaller/pyinstaller>

## Inno Setup

- O instalador é gerado pelo Inno Setup; os termos do Inno Setup se aplicam ao
  compilador e à distribuição do instalador.
- Projeto: <https://jrsoftware.org/isinfo.php>

## Regra de empacotamento

O pacote público deve manter estes avisos, os textos de licença aplicáveis e
os links de código-fonte correspondentes. Nenhum arquivo de terceiro deve ser
apresentado como código proprietário do Netrunner Studio.
