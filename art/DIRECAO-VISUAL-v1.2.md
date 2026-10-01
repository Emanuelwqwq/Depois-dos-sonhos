# Depois do Sono 1.2 — jardim entre mundos

Direção escolhida: dreamcore mais estranho, com espaços vazios, névoa e elementos surreais. Aero mantém água e tons claros, compartilhando o acabamento da primeira região.

## Implementado
- Novas texturas de musgo frio, pedra, piso quadriculado e água, criadas com ImageGen.
- Quatro elementos ilustrados com ImageGen: porta isolada, janela suspensa, escada sem destino e relógio lunar. Distribuição procedural reproduzível, com centros e saídas livres para combate.
- Menos canteiros e caminhos mais estreitos; vegetação pequena em uma camada nítida, desenhada uma vez. O chão continua armazenado em textura para reduzir trabalho por quadro.
- Névoa leve, ondulações na água, partículas discretas e flutuação lenta de objetos. A névoa fica atrás dos personagens e da interface. O relógio ambiental acompanha a partida, parando na pausa; movimento reduzido congela a animação ambiental.
- Rastros de projéteis mais simples e definidos, pequenos clarões de impacto e menos sobreposição de efeitos. Hitboxes e equilíbrio de combate preservados.

## Limites desta entrega
Validação automática: 12.248 verificações passaram, incluindo simulação completa de campanha, balanceamento, coleção, coop, duelo, interface, animações e 11 verificações específicas da arte nova. Capturas das duas regiões e vídeo de 10 segundos renderizados no Godot foram revisados.

Esta atualização muda materiais, composição e movimento do cenário. Mantém as folhas de personagens e inimigos revisadas na 1.1; não promete redesenho completo de todas as skins nem novos quadros direcionais para todas as ações.

Teste de carga local: Intel UHD, 63 inimigos e cerca de 48 projéteis. Mediana de 25,59 ms/quadro, p95 de 36,11 ms. Uma execução de controle sem névoa visível e sem vegetação baixa teve mediana de 23,11 ms e p95 de 36,23 ms. São medições desta sessão, com outros aplicativos abertos; não garantem 60 FPS nem desempenho em celulares. A medição antiga da 1.1 ocorreu em condições diferentes e não permite atribuir toda a diferença à arte nova.

Android físico, controle físico, rede externa e iPhone continuam sem validação nesta máquina. A versão Android é um APK de teste assinado pela chave local existente. iPhone exige ambiente Apple e assinatura.
