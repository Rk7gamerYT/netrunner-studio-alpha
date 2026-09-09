# Netrunner Studio — Alpha 0.4.2

Netrunner Studio é um estúdio de produção ao vivo para Windows, com canvas
horizontal 16:9 e vertical 9:16, preview ao vivo, cenas, fontes, mixer de
áudio, transições, controles e captura de tela/janela.

Esta página é o canal público para testers. O instalador não exige Python nem
uma instalação separada do OBS na variante alpha bundled.

A build A_0.4.2 atual usa Nuitka standalone com PySide6/Qt 6.10.1. O ciclo
instalar → abrir → iniciar o host nativo → fechar → desinstalar foi validado
no Windows 11 antes da publicação.

## Download

Baixe `NetrunnerStudio-Alpha-Setup-0.4.2.exe` na seção **Releases** e confira
o SHA-256 publicado junto do arquivo antes de executar. Esta versão ainda é
alpha e pode conter bugs; reporte problemas com passos para reproduzi-los.

As capturas serão atualizadas depois da rodada atual de correções visuais; a
Release prioriza o instalador funcional e não usa imagens antigas de
desenvolvimento como se fossem a interface final.

## Licenças

O código próprio do Netrunner Studio não é publicado neste repositório. Os
avisos e links das dependências de terceiros estão em
[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md). A distribuição bundled
inclui o runtime do OBS Studio e sua licença GPLv2 correspondente.
