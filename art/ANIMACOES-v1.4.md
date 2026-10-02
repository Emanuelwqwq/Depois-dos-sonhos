# Depois do Sono 1.4 — gestos de cada hóspede

## Animações

- Os oito protagonistas e suas 40 roupas agora têm esquiva, habilidade, dano e derrota voltados para frente e costas. São 96 folhas novas, 384 sequências e 2.314 quadros gerados com ImageGen. As vistas laterais preservam as animações de perfil existentes.
- Repouso e caminhada têm ritmo próprio por personagem: pausas sonolentas da Nuvem, passos mais rápidos do Pipo, preparação e pouso do Nilo, entre outros. O período total da caminhada continua associado à distância percorrida.
- Esquivas duram 0,32 s, apresentação de habilidade 0,8 s, reação de dano 0,18 s e queda 0,9 s. A última pose de derrota permanece parada. Esses tempos de apresentação não alteram alcance, dano, hitboxes ou invencibilidade.
- As poses de queda usam a altura do quadro em pé como referência, evitando que o corpo cresça ao deitar. Os recortes preservam o PNG original e usam a transparência para separar os quadros.
- Refeitos os ataques da água-viva, sentinela de escudo e louva-a-deus do Aero, retirando cortes nas bordas dos efeitos.
- Corrigido o compartilhamento dos dados de desenho no cooperativo: o segundo jogador também recebe origens, alturas e fontes das novas poses.

## Validação

- 27.438 verificações na suíte completa, sem falhas; incluem combate, ondas, compras, progressão, guarda-roupa, cooperativo, arena e animações.
- 96 folhas e 2.314 quadros conferidos quanto a transparência, limites e bordas opacas; três ataques Aero verificados separadamente.
- 384 cenas renderizadas no Godot com os dois jogadores, abrangendo todas as aparências, as quatro ações e as duas direções. Sem erros de renderização registrados. Prévias e capturas de frente/costas inspecionadas.
- Teste de carga em Intel UHD: 63 inimigos e 48 projéteis, mediana de 16,67 ms, p95 de 18,06 ms e p99 de 25 ms. A medição anterior da 1.3 teve p95 de 16,67 ms; esta execução apresentou mais variação. Os resultados não substituem testes em celulares.
- A revisão automática de recortes e seleção de poses não certifica perfeição artística de todas as transições. O vídeo da versão permite conferir exemplos no ritmo real.
- EXE exportado iniciado e encerrado sem erros nesta máquina. APK exportado com assinatura v2/v3 e alinhamento de 16 KB verificados; instalação em aparelho físico não realizada.

## Instalação e limites

Windows incorpora os recursos no EXE. Android mantém o pacote e a chave de teste existentes, com versionCode 20. Compras, skins e preferências continuam com suas chaves de save. Ambos os participantes devem usar a versão atual no multiplayer.

Android físico, controle físico e conexão entre redes externas continuam sem validação nesta máquina. iPhone exige ambiente Apple e assinatura; não acompanha instalador iOS.

## Reprodução e fontes

Catálogos: `art/actions14.json` e `art/reactions14.json`. Prompts e resultados individuais estão nos arquivos `*_actions14*` e `*_reactions14*` de `art`. Os três ataques usam `tools/index_enemy_attacks14.py`. Arquivos finais em `assets/sprites`; metadados em `motion_atlas.json`.

Validação: `tools/verify_actions14.py`, `tests/animation14.gd`, `tests/coop6.gd`, `tests/animation14_preview.gd` e `tests/animation14_combat_capture.gd`. Os PNGs foram gerados com o ImageGen integrado; a indexação calcula recortes e posições, sem redesenhar pixels por código.
