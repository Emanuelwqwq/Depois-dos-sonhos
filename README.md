# Depois do Sono — versão 0.7

Survivor nativo em Godot 4.6/GDScript para Windows e Android. Dreamcore nas ondas 1–20, Frutiger Aero nas ondas 21–40, oito protagonistas, 40 roupas com habilidades de campanha, 17 armas e 20 power-ups.

[Downloads da versão 0.7](https://github.com/Emanuelwqwq/Depois-dos-sonhos/releases/tag/v0.7) • [Guia multiplayer](MULTIPLAYER.md) • [Validação](art/VALIDACAO-v0.7.md)

Numeração atual: **0.7**, com próximas atualizações em **0.8, 0.9, 1.0**. Veja [versionamento](VERSIONAMENTO.md).

## Novidades

- Cooperativo para dois e arena PVP, no mesmo PC ou por rede direta. Descoberta de salas na mesma rede Wi-Fi, sem contratar servidor. Fora da rede local não há relay nem conexão automática por convite.
- Animações de repouso, movimento, esquiva/habilidade, dano e derrota para os oito protagonistas e todas as 40 roupas. Inimigos e chefes das duas regiões têm movimento, preparação, ataque, dano e morte.
- Reprodução mais lenta: caminhada a 7 quadros por segundo, repouso a 3. A velocidade visual não aumenta o tempo de invencibilidade. Hitboxes continuam independentes da arte.
- Trilhas curvas, partículas e quatro sequências ilustradas de efeitos para armas. Limites de efeitos, descarte fora da câmera e carregamento de folhas sob demanda.
- Frente e costas para repouso e caminhada dos oito protagonistas e todas as 40 roupas. A Sala de Ensaio permite conferir cada direção. Esquiva, habilidade, dano e derrota preservam poses de perfil em três quartos.
- Uma quinta roupa por personagem: Coraline, Pequeno Príncipe, Felix/Ferris, Leon, Marceline, Armadilha de Urso Reversa, Puck e Wirt, cada uma com habilidade de campanha própria.
- Yoshikage Kira substitui a segunda roupa da Lua, preservando a compra existente. Nilo usa uma armadilha de metal industrial escuro; Puck tem pelagem cinza-clara, peito branco e olhos azul-esverdeados.
- Novos retratos na loja, recortes de animação revisados e efeitos específicos das habilidades. Para jogar em rede, ambos precisam desta versão (protocolo 7).

## Jogar

PC: abra `Jogar.cmd` ou `build/DepoisDoSono-v0.7.exe`. Os recursos estão incorporados ao executável. Android: instale o APK da release, em paisagem. O pacote Android continua sendo uma compilação de teste assinada com a chave local existente. Não há IPA para iPhone; veja [preparação iOS](IOS.md).

| Ação | Teclado/mouse | Controle | Android |
|---|---|---|---|
| Movimento | WASD/setas ou clique no chão | Analógico/direcional | Joystick esquerdo |
| Ataque | Automático | Automático | Automático |
| Esquiva | Espaço/clique direito | A/RB | Botão Esquiva |
| Habilidade | E/botão central | X/LB | Botão Habilidade |
| Pausa | Esc | Start | Botão de pausa |

No cooperativo local, as setas ficam com J2; V esquiva e B usa sua habilidade. Com um controle conectado, ele fica com J2. Detalhes de conexão, compras em dupla e arena estão em MULTIPLAYER.md.

## Campanha e equilíbrio

Ímã dura oito segundos e atrai também cacos novos. Um único ímã por vez, intervalo mínimo de 25 segundos e queda condicionada a cacos no chão. Pausar também pausa seus efeitos.

A dificuldade adapta frequência de surgimento e limite de comuns entre 75% e 115%, preservando atributos e ataques dos inimigos. As duas primeiras ondas mantêm o padrão introdutório. Limites iniciais: 24 comuns na onda 1, 60 na 20 e 80 na 40. Bosses reduzem o surgimento dos comuns.

Experiência acumulada é separada da carteira. Primeira melhoria em 20 pontos; os próximos intervalos seguem `20 + 10 × nível + nível²`. Comprar não apaga experiência; preços crescem com onda, compras, raridade e nível do item. Armas têm cinco níveis e quatro espaços; comprar com inventário cheio abre escolha explícita de substituição.

Compras permanentes, roupas e histórico antigo são preservados. Recordes do equilíbrio revisado ficam separados. A pausa apresenta os equipamentos; bestiário revela apenas encontros vistos. Configurações permite reduzir detalhes visuais.

## Desenvolver e exportar

Abra `project.godot` no Godot 4.6. `build-windows.ps1` roda as suítes e exporta Windows; `build-android.ps1` exporta e verifica assinatura e alinhamento do APK. Ferramentas locais ficam em `.tools`, fora do pacote de código-fonte. Testes de rede usam duas instâncias e estão em `tests/network6.gd` e `tests/network_menus6.gd`.

A prévia exige testes em Android e controles físicos. As verificações automatizadas de rede ocorrem no mesmo computador, não em uma rede móvel real. Não há suporte validado a iPhone sem ambiente Apple e assinatura.
