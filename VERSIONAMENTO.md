# Numeração das versões

A versão atual é **0.6**. A pedido do autor, as próximas atualizações públicas seguem **0.7, 0.8, 0.9, 1.0, 1.1**, sempre em incrementos de **0.1**.

Manter a versão coerente em `project.godot`, nomes de exportação, `export_presets.cfg`, `Jogar.cmd`, `tools/package_release.py`, README e tag do GitHub (`v0.6` atualmente).

O contador interno de instalação Android é independente e deve sempre aumentar, mesmo quando o nome público muda. A versão 0.6 usa `versionCode=12`, preservando a possibilidade de atualizar o APK anterior, de nome 6.1.0-preview.1 e código 11. Preservar o identificador do pacote e a chave de assinatura.

As releases antigas ficam como histórico. A versão pública 0.6 substitui a nomenclatura anterior; não corresponde a uma reversão do jogo ou dos saves.
