# Multiplayer — versão 1.0, experimental

Dois jogadores podem participar da campanha cooperativa ou de uma arena PVP separada, no mesmo PC ou por conexão direta. Use a mesma versão nos dois aparelhos.

## Caminho mais simples: mesma rede

1. Abra Multiplayer e escolha Cooperativo ou Arena PVP.
2. No anfitrião, escolha personagem e crie a sala na rede.
3. No outro aparelho, escolha personagem e Encontrar na rede. Toque na sala encontrada.
4. A partida começa quando o convidado se conecta. No PVP, escolha também sua arma antes de entrar.

Se a busca não encontrar a sala, digite o IP local mostrado pelo anfitrião. Os aparelhos precisam se alcançar pela rede; redes de convidados podem isolar dispositivos. O Windows pode pedir acesso à rede para o jogo. Portas: UDP 27771 para a partida, UDP 27772 para descoberta.

Não é necessário contratar servidor para esse caminho. Não há relay, código de convite pela internet nem travessia automática de NAT. Fora da mesma rede, o IP precisa estar acessível; alguns roteadores exigem encaminhamento da porta UDP 27771 e conexões sob CGNAT podem impedir hospedagem direta. Não foi validada conexão entre redes externas nesta entrega.

## Mesmo PC

Selecione os personagens e Jogar neste PC. Um controle conectado fica com J2; dois controles ficam separados entre J1 e J2. Sem controles, J1 usa WASD, Espaço e E; J2 usa setas, V e B. Mouse/toque operam J1 e os botões dos menus. Ataques das armas são automáticos.

Controle: analógico/direcional move; A/RB esquiva; X/LB usa habilidade; Start pausa. Na escolha de melhorias, direcional seleciona, A confirma, B cancela substituição e Start confirma que está pronto na loja. Cada jogador tem seu painel.

## Campanha em dupla

- Câmera compartilhada, afastamento máximo de 600 unidades.
- Cada caco concede dinheiro e experiência aos dois uma única vez. Inventários e compras individuais. Ambos escolhem antes de seguir.
- Para reviver um aliado caído, permaneça perto dele por três segundos sem receber dano. Ele volta com 35% da vida e um segundo de proteção. A partida acaba quando ambos caem.
- Comuns têm 1,6× de vida e chefes 1,8×. O limite de inimigos e o dano não são multiplicados. A adaptação considera os dois participantes.
- A pausa interrompe o mundo para ambos. Desconexão do convidado pausa o anfitrião; na campanha ele pode continuar sozinho. Não há reconexão automática ou migração de anfitrião.

## Arena PVP

Melhor de três rounds, com três segundos de preparação e até dois minutos por round. Vence quem derrotar o oponente; no tempo limite, vence a maior proporção de vida. Empates vão para uma área segura que encolhe.

Vida, velocidade, defesa e níveis de arma são padronizados. As oito classes têm habilidades próprias para a arena. Skins são cosméticas neste modo. Não há cacos, experiência ou progresso competitivo permanente. O anfitrião tem autoridade; esta prévia não oferece ambiente competitivo protegido contra trapaças.

## Implementação e limites

CoopSession coordena dois estados de jogador e um mundo. NetworkSession usa ENet: simulação autoritativa a 30 Hz, estados a 15 Hz, fragmentos comprimidos de até 1000 bytes, ordenação e interpolação visual. O convidado envia comandos; dano, drops e compras são calculados no anfitrião. Não há previsão local/reconciliação; latência alta aumenta a demora percebida no controle.

Testes automatizados usam dois processos reais de Godot no mesmo computador, incluindo descoberta por loopback, movimento, habilidades, melhoria, pausa e desconexão. Isso não substitui testes PC↔Android em Wi-Fi, controle físico, perda de pacotes, internet externa ou aplicativo em segundo plano. Android inclui permissão INTERNET; validação física permanece pendente.

A arquitetura usa recursos disponíveis no Godot para iOS, mas não há IPA: ainda são necessários Mac, Xcode, assinatura Apple e testes em iPhone. Veja IOS.md.

## Conteúdo da versão 1.0

Protocolo 10. Eventos opcionais são simulados pelo anfitrião e sincronizados; a recompensa de XP vai para os dois, sem cacos extras. Cada participante escolhe sua evolução. Ressonâncias e evoluções especiais não se aplicam ao PVP.
