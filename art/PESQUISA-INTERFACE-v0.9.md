# Pesquisa e proposta de interface — Depois do Sono

27/09/2026. Etapa de pesquisa solicitada pelo usuário; nenhuma alteração no jogo ou publicação nova. Proposta para a próxima revisão, ainda sujeita a protótipo e teste.

## Referências consultadas

Pesquisa documental em páginas oficiais, notas de atualização e capturas indexadas de seis jogos. Não houve sessão prática nesses jogos nem medição de tempos de seus alertas. Capturas de versões diferentes não comprovam comportamento animado. Os limiares e durações abaixo são propostas nossas.

| Referência | Evidência e aplicação proposta |
|---|---|
| [Brotato](https://store.steampowered.com/app/1942280/Brotato/) | Separa combate em ondas das compras entre ondas. Usar essa separação para retirar detalhes de equipamento do combate e tornar a loja comparável. As [notas oficiais de dezembro de 2023](https://store.steampowered.com/news/posts/?enddate=1701771597&feed=steam_community_announcements) registram opções de opacidade para projéteis/explosões e correção da barra de vida escondida por efeitos: prioridade de desenho importa tanto quanto cor. |
| [Vampire Survivors](https://poncle.itch.io/vampire-survivors) | Referência de combate com pouca interação de menu; a página do desenvolvedor registra melhorias no feedback de receber dano. Separar claramente dano momentâneo de perigo persistente. [Galeria de gameplay](https://steamcommunity.com/app/1794680/screenshots/) como referência de distribuição compacta dos indicadores. |
| [20 Minutes Till Dawn](https://store.steampowered.com/app/1966900/20_Minutes_Till_Dawn/) | Capturas mostram corações e poucos indicadores destacados. Aproveitar a leitura por formas simples e a paleta limitada; manter barra numérica em Depois do Sono, pois a vida máxima e o dano variam. [Referência com capturas](https://store.epicgames.com/en-US/news/20-minutes-till-dawn-guide-how-to-survive-and-thrive-at-the-highest-difficulties). |
| [Death Must Die](https://store.steampowered.com/app/2334730/Death_Must_Die/) | A [galeria de gameplay](https://steamcommunity.com/app/2334730/screenshots/) apresenta vida, retrato e comandos agrupados na parte inferior. Referência para concentrar informações relacionadas e reduzir caixas dispersas; adaptar a posição para os dedos no celular. |
| [Halls of Torment](https://steamcommunity.com/games/2218750/announcements/detail/3708207677659565414) | Atualização de 21/09/2023 separa armas/itens nas informações, marca habilidades melhoradas com pequenos sinais e melhora contraste dos projéteis. Aplicar categorias claras na pausa, níveis discretos nos ícones e contraste em Jardim e Aero. [Transcrição acessível das notas](https://steamdb.info/patchnotes/12245146/). |
| [Keeper's Toll](https://steamcommunity.com/app/2002220/discussions/0/599638172337546851/) | O desenvolvedor confirma que o personagem piscava em vida baixa, mas jogadores não percebiam. Depois adicionou um overlay opcional em acessibilidade, ativado a 50% naquela atualização. Usar alerta redundante e configurável; não assumir que 50% é adequado ao nosso equilíbrio. |

## Diagnóstico da versão 0.8

O HUD atual usa caixas de fundo semelhantes para informações de importância diferente. O retrato e os textos ocupam bastante espaço enquanto a barra de vida tem só nove unidades de altura. Botões grandes de habilidade/esquiva permanecem no PC; textos de tutorial, nome da habilidade e descrições curtas competem com o combate.

O alerta atual repete texto em vários lugares, desenha uma moldura retangular fina e usa um toque de sino genérico. A alteração do rosa da vida para coral é pouco distinta. A placa sobre o cenário adiciona ruído, mas não garante reconhecimento imediato do perigo. Esta é uma avaliação do nosso código/interface e do relato do usuário.

## Direção visual proposta

Hotel dos Sonhos com interface leve: noite azul, creme e latão discreto; pequenas chaves, luas e etiquetas nos pontos de navegação. Ícones desenhados como uma família consistente. Títulos com personalidade nos menus; números e comandos com fonte simples e legível. Evitar moldura dourada e bloco azul em todos os elementos.

No combate, usar vida em barra compacta com número e pequeno símbolo de lua/coração; experiência em linha fina separada, marcada XP e nível. Onda e tempo centralizados sem cartão grande; cacos e pausa num canto. Quatro armas em uma fileira curta com níveis discretos. Habilidade e esquiva mostram ícone e recarga, com teclas/botões correspondentes ao dispositivo. Buffs temporários mostram apenas ícone e duração. Explicações ficam disponíveis na pausa por mouse, toque e controle.

Em PC/controle, testar vida e ações agrupadas na faixa inferior. Em celular, manter vida no alto e ações ao alcance do polegar, com áreas de toque confortáveis. Não reduzir alvos de toque apenas para parecer minimalista. A região Aero muda acabamento/cor secundária sem mover controles. No cooperativo local, identificar J1/J2 por nome e forma, além da cor.

Menu inicial: cenário animado como protagonista, Jogar em destaque, navegação curta. Seleção e guarda-roupa: grande retrato, lista organizada e habilidade legível. Loja: ofertas lado a lado, preço, benefício e comparação explícita com a arma substituída. Pausa: categorias Armas, Habilidade, Power-ups e Efeitos. Morte/vitória: resultado, motivo da morte quando disponível e ações claras. Configurações: seções curtas, escala da interface, movimento e intensidade dos alertas.

## Alerta de vida: protótipo proposto

- Ao sofrer dano: resposta curta no personagem e trecho de vida perdida que desaparece suavemente na barra; som próprio de impacto.
- Até 35%: barra local curta aparece perto do personagem, acima de efeitos e sem painel de texto; pequeno símbolo de perigo e um aviso sonoro ao entrar nesse estado.
- Até 20%: pulso lento na barra e vinheta suave somente nas bordas, mantendo personagem, projéteis e controles legíveis. Batimento curto e espaçado, diferente de coleta/cura.
- Retorno acima de 40%/25%, respectivamente, encerra cada alerta; essa margem evita liga/desliga constante por regeneração. Pausa suspende pulso e áudio; morte encerra o alerta.
- Som, vinheta e vibração ajustáveis. Opção de reduzir movimento mantém forma e contraste estáticos. Não depender só do vermelho, nem aplicar tremor, desfoque ou flashes de tela inteira.
- No cooperativo local, o perigo do parceiro deve ser identificado na barra dele e junto ao personagem; evitar uma tela inteira em alerta sem indicar quem está em risco.

35% e 20% são valores iniciais para avaliação, não uma cópia de outro jogo nem mudança já implementada.

## Implementação posterior

1. Protótipos do HUD em vida normal, ferido e crítico, tanto no Jardim quanto em Aero; PC, celular e cooperativo.
2. Comparar os protótipos com o HUD 0.8 em cenas com muitos inimigos e efeitos. Verificar reconhecimento da vida crítica sem ler texto, com som ligado e desligado.
3. Implementar a família de componentes e adaptar todas as telas, começando pelo combate e a loja.
4. Testar controles, textos longos, proporções de tela, escala, contraste, pausa, cura oscilante e sobreposição de efeitos. Medir desempenho no mesmo cenário antes/depois; validação em aparelho físico continua necessária.
5. Gerar os pacotes da próxima versão somente depois dessa validação.
