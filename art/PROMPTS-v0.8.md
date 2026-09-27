# Arte — versão 0.8

Retratos dedicados à loja, produzidos com ImageGen integrado em 27/09/2026, usando as folhas de animação aprovadas como referência de identidade e a coleção antiga como referência de acabamento. As animações existentes foram preservadas.

- `portraits08_a.png`: Lua/Kira, Nilo/Armadilha de Urso Reversa, Nuvem/Puck. 1944 × 809. Prompt em `prompt-portraits08-a.md`.
- `portraits08_b.png`: Íris/Coraline, Noé/Pequeno Príncipe, Lua/Felix. 2172 × 724. Prompt em `prompt-portraits08-b.md`.
- Recortes transparentes em `assets/sprites/portraits08.json`, entre 535 e 616 pixels de largura e 574 a 698 de altura. A loja usa esses retratos em vez dos pequenos quadros de animação.

## Pendência explícita

**Bento/Leon, Rubi/Marceline e Pipo/Wirt** ainda usam as imagens anteriores. O ImageGen retornou `usage_limit_reached` antes de gerar o terceiro grupo. Não foram substituídos por desenhos de outro estilo. É necessário retomar a geração quando a cota liberar.

Prompt previsto: criar uma folha transparente horizontal com três retratos completos em alta definição, na ordem Bento/Leon, Rubi/Marceline e Pipo/Wirt. Usar `bento_skin5_motion.png`, `rubi_skin5_motion.png` e `pipo_skin5_motion.png` como referências de identidade, e `skins_1.png` como referência de acabamento. Preservar espécie, roupa, paleta e proporções. Uma pose relaxada em três quartos por personagem, corpo inteiro, sem cortes, texto, sombras de chão ou cenário. Contornos limpos, olhos nítidos, texturas suaves e detalhes de tecido; personagens separados em três colunas com margens transparentes. Pelo menos 600 pixels de altura por retrato.

## Alinhamento

`tools/index_actor_anchors.py` apenas mede a transparência das folhas e grava âncoras no índice JSON; não redesenha nem altera pixels. Execute-o depois de reconstruir `motion_atlas.json`. O motor usa as medidas para estabilizar a base e o tamanho de repouso e caminhada em todas as 48 aparências e três vistas.
