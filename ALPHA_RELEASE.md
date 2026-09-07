# Netrunner Studio A_0.4 — checklist de release alpha

## O que já está pronto

- PyInstaller em modo `onedir`: o usuário final não precisa ter Python
  instalado.
- UPX desativado para reduzir heurísticas de antivírus sobre executáveis
  comprimidos.
- Metadados de versão e produto no executável.
- Inno Setup por usuário, sem exigir administrador.
- Layout dos painéis versionado: instalações antigas não restauram geometrias
  obsoletas ou sobrepostas.
- Avisos de terceiros separados do código proprietário.

## Gates antes de publicar

1. Manter PySide6 na opção LGPL e revisar os avisos de terceiros antes de
   publicar.
2. Definir o endereço/repositório oficial onde o código-fonte do OBS e os
   avisos serão disponibilizados.
3. Assinar o instalador e o executável principal quando houver certificado de
   assinatura de código. Sem dinheiro para certificado, publicar HTTPS,
   SHA-256 e os avisos é a alternativa honesta, mas não elimina o SmartScreen.
4. Testar em uma máquina limpa, sem Python, PyQt ou OBS pré-instalados quando
   a variante bundled for escolhida.
5. Submeter os hashes e o instalador aos portais de reputação do antivírus,
   quando disponíveis.

Assinatura digital reduz alertas de reputação, mas não garante que nenhum
antivírus fará uma detecção. Certificado autoassinado não resolve o problema
para usuários finais.
