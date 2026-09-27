# Validação — Depois do Sono 1.0

27/09/2026. Godot 4.6, Windows e Android; incremento 0.9 → 1.0.

## Implementado
- Quatro ressonâncias: Subaru/Mão Invisível; Íris Vaporeon/Pulso da maré; Bento Denji/Cordinha; Pipo Gengar/Riso de sombra. Independentes por jogador, excluídas do PVP, descritas no guarda-roupa/loja/pausa.
- Quatro sinergias de equipamento; três power-ups novos de uma cópia, com ícones ImageGen e transparência. Cura gera carga somente pela regeneração efetiva de Chá + Margarida, limitada a uma descarga.
- Duas evoluções por arma no nível 5, custos iguais, escolha mutuamente exclusiva. Cadência: 1,3× frequência, 0,85× dano; Eco: 0,5× dano em área a cada três disparos. Sem alterar preços progressivos.
- Três desafios opcionais nas ondas terminadas em 3, apresentados como portas: defesa, perseguição de mariposa e luzes na névoa local. Sem viagem para mapa separado. Prazo 22s; defesa pede 10s livres de inimigos, com 6s de tolerância a invasões. Outros pedem três aproximações. Recompensa 20+onda XP, limitada a 40, e 8 de cura. Nenhum caco adicional. Falha não bloqueia a partida. Pactos antigos preservados nas ondas terminadas em 2.
- Mãe das Mariposas e Baleia do Horizonte revisadas: aviso de 1,4s, disparo regional e recuperação a partir de 3s, ciclo total de 5,4s. Mariposa deixa duas aberturas no leque; baleia marca um anel com centro seguro. Recuperação recebe 20% mais dano. HP em coop mantém multiplicador 1,8.
- Animações existentes refinadas com transição de 0,12s repouso/caminhada e cadência por distância, âncoras preservadas, tempo negativo corrigido. Chefes sincronizam preparação/ataque/recuperação. Não foram redesenhados todos os quadros nesta revisão.
- Efeitos por família de projétil, impactos curtos com limite de 40 efeitos para novos pequenos brilhos, cores de perigo preservadas e descarte visual fora da câmera.

## Testes
6714 verificações aprovadas somando suites: smoke 301, expansion 156, guest_collection 154, gameplay4 238, balance5 4898, coop6 14, duel6 34, directions6 768, collection7 63, revision8 23, interface9 12, resonance10 17 e revision10 36. A última suite foi ampliada após a execução completa e rodada novamente; gameplay4 também passou após os últimos ajustes de combate.

Simulação completa: 39198 passos, 9116 inimigos derrotados, sem travamento de conclusão. Testes cobrem migração de save, invencibilidade, alcance, coleta, adaptação, pausa, transição Aero, skins, escolhas e substituição de armas. Novos testes cobrem recompensas únicas, XP separado de dinheiro, falha/pausa de eventos, compra exclusiva de evolução, recuperação de bosses e bônus por roupa.

Coop e PVP executados entre dois processos em 127.0.0.1: conexão, movimento e habilidade sincronizados. Protocolo 10; instalação antiga não é compatível na mesma sessão. Campos de evento e disponibilidade replicados pelo anfitrião.

Revisão visual: telas de evolução, três novos itens, pausa com ressonância, guarda-roupa, evento com controles de toque simulados e boss Aero. Layouts 960×600 e 1600×720 renderizados no PC. Arte de ícones validada em atlas com alpha; roupas e folhas direcionais existentes preservadas.

## Desempenho medido
Intel UHD Graphics, OpenGL Compatibility, cenário reproduzível de performance: 63 inimigos e 48 projéteis ao fim, 479 amostras. Mediana de quadro 16,67ms; p95 16,69ms; p99 18,06ms. Simulação p95 1,94ms, desenho p95 5,70ms. Uma rodada anterior durante preparação/exportação marcou p95 23,60ms; efeitos pequenos foram simplificados e a medição repetida. Comparação não isola toda a carga do sistema e não é promessa para outros aparelhos.

## Pacotes e limitações
EXE com recursos incorporados. APK de teste assinado com a chave local existente, versionCode 16, versão 1.0, pacote preservado. Assinatura v2/v3 e alinhamento 16KiB verificados. Fonte ZIP exclui SDKs, chaves, saves e caches; SHA256 acompanha a release.

Sem validação em aparelho Android físico, controle físico ou internet entre redes diferentes. Toque foi simulado no PC. iOS continua sem IPA: precisa de ambiente Apple e assinatura. Os retratos ampliados anteriormente pendentes de Leon, Marceline e Wirt não fazem parte desta revisão.
