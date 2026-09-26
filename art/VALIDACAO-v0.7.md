# Validação — Depois do Sono 0.7

Data: 26/09/2026. Godot 4.6, Windows. Android versionName 0.7 / versionCode 13.

## Alterações

40 roupas: cinco por personagem. Lua recebeu Kira no lugar da segunda roupa, mantendo a chave de compra 2:2, e Felix/Ferris como quinta. Novas quintas roupas: Coraline, Pequeno Príncipe, Leon, Marceline, Armadilha de Urso Reversa, Puck e Wirt. Nilo usa metal industrial escuro e mandíbulas articuladas; Puck usa cinza-claro, branco e olhos azul-esverdeados.

Nove folhas de perfil e nove de frente/costas produzidas com ImageGen integrado. 48 aparências totais (oito originais e quarenta roupas) têm repouso e caminhada de frente e costas. Outras ações mantêm o perfil. Recortes revisados no motor; linhas com sete poses têm limites próprios. A recuperação de esquiva de Marceline reutiliza sua pose limpa de agachamento, evitando uma pose sobreposta na folha original.

Habilidades novas têm limites explícitos: Kira detona após aviso, rosa bloqueia até oito tiros, Felix exige permanecer no ponto de canalização, Marceline produz três pulsos, Nilo limita o bônus a seis eliminações, Puck exige três pulsos e respeita resistência dos chefes, Wirt marca até quatro alvos por pulso. Efeitos específicos e descarte fora da câmera. Skins permanecem cosméticas no PVP.

## Verificações automatizadas

| Suíte | Resultado |
|---|---:|
| Campanha completa / smoke | 301/301 |
| Expansão e preços | 156/156 |
| Compra e persistência das roupas | 154/154 |
| Armas, controles e habilidades | 238/238 |
| Equilíbrio, coleta e limites dos atlas | 4898/4898 |
| Cooperativo | 14/14 |
| Arena | 34/34 |
| Frente e costas / seleção de quadros | 768/768 |
| Mecânicas novas, limites e migração Kira | 63/63 |
| Total | 6626/6626 |

Simulação completa: 38.391 passos, 9.133 inimigos derrotados, cerca de 20 segundos de execução sem renderização. Não representa FPS de aparelho físico.

Duas instâncias locais conectadas: skin Felix/Ferris reconhecida, caminhada frontal e traseira recebidas pelo anfitrião e cliente. Protocolo 7 exige a mesma versão nos dois participantes.

Galerias renderizadas no Godot, revisão visual dos novos perfis em três momentos e das telas de Nilo, Puck e Kira. Compra da quinta roupa corrigida e testada; compras antigas preservadas. Logs e capturas locais em build.

Windows exportado com sucesso; executável inicia e encerra sem erro no teste headless. APK identifica pacote com.depoisdosono.game, versão 0.7, código 13; assinatura v2/v3 e alinhamento de 16 KiB aprovados. Chave de assinatura existente preservada.

## Limites da validação

Sem teste físico nesta entrega em Android, controles, rede móvel ou ligação PC–Android. Rede automatizada testada no mesmo computador. Não há relay para conexão automática fora da LAN. Sem Mac/Xcode e assinatura Apple, não foi gerado IPA. O APK continua sendo uma compilação de teste assinada com a chave local existente.

Downloads: [release v0.7](https://github.com/Emanuelwqwq/Depois-dos-sonhos/releases/tag/v0.7). Prompts: [PROMPTS-v0.7.md](PROMPTS-v0.7.md). Código-fonte completo no Projeto-v0.7.zip; ferramentas locais, saves e chaves não são incluídos.
