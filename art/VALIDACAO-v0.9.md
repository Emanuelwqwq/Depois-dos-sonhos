# Depois do Sono 0.9 — interface e percepção de perigo

27/09/2026. Godot 4.6. Windows e Android (código 15). Protocolo de rede 8 preservado.

## Implementado

HUD refeito em componente separado, com menos área coberta. Vida/experiência ficam na faixa inferior no PC e no alto no modo de toque. Indicadores compactos de armas, onda, tempo e cacos; botões menores no PC, preservando áreas de toque no Android. Cooperativo identifica os dois hóspedes; arena usa a mesma apresentação de vida.

Botões e painéis compartilham acabamentos mais discretos em menu, seleção, loja, guarda-roupa, bestiário, pausa e resultados. Menu tem rótulos mais curtos. Troca de armas mostra alcance atual e alcance da oferta. As compras continuam individuais no cooperativo e não tiveram preços alterados.

Vida baixa em 35%; crítica em 20%. Retorno acima de 40%/25% evita oscilação por cura contínua. Barra junto ao personagem e símbolo de perigo aparecem acima da renderização de inimigos e efeitos; o trecho de vida perdida fica visível brevemente. Em situação crítica solo há bordas suaves e pulso lento. No cooperativo, o aviso individual identifica quem está em risco.

Batimento original curto, pré-gerado, com voz de áudio dedicada para não ser interrompido por coleta. Intervalo de 3,2 segundos em estado crítico; som ao entrar no perigo. Pausa suspende contadores e interrompe o som; morte limpa o estado. Configurações persistem som de perigo, bordas e movimento reduzido. Movimento reduzido retira tremor de câmera e animação de fundo do menu, mantendo avisos estáticos.

## Testes

6.649 verificações anteriores passaram: campanha completa (301), expansão (156), roupas (154), controles/armas (238), equilíbrio/atlas (4898), cooperativo (14), arena (34), direções (768), coleção (63) e revisão 0.8 (23).

12 verificações novas em interface9.gd passaram: entrada e saída de perigo/crítico, margens de recuperação, morte, rastro de dano, estabilização, persistência de preferências e congelamento na pausa. Total: 6.661 verificações.

Capturas no Godot para HUD normal/crítico, modo de toque, cooperativo, Aero, loja, pausa, configurações, guarda-roupa, morte, seleção, bestiário e arena. Simulação de toque é uma inspeção de layout no PC, não validação em telefone. Registros em build/ui09-*.png e logs locais.

Pacotes exportados com sucesso. APK identifica com.depoisdosono.game, versão 0.9/código 15; assinatura v2/v3 e alinhamento de 16 KiB verificados. Windows iniciou sem erro no teste headless. A inspeção final também confirma o joystick na arena em modo de toque.

## Limitações e pendências

Não houve teste físico de Android, controle ou rede PC–Android nesta entrega. Não foi medido FPS em aparelho móvel. A nova interface usa geometria simples e recursos compartilhados; a percepção dos alertas ainda deve ser avaliada pelo jogador em partidas reais.

Não foram produzidos retratos novos nesta revisão: Leon, Marceline e Wirt permanecem com as imagens anteriores. iPhone continua sem instalador, pois exige ambiente Apple e assinatura. APK usa a mesma chave de teste das versões anteriores. Saves e compras mantêm as chaves existentes.

Pesquisa que orientou a revisão: [PESQUISA-INTERFACE-v0.9.md](PESQUISA-INTERFACE-v0.9.md). [Downloads](https://github.com/Emanuelwqwq/Depois-dos-sonhos/releases/tag/v0.9).
