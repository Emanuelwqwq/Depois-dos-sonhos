# Validação — Depois do Sono 0.8

Data: 27/09/2026. Godot 4.6, Windows. Android versionName 0.8 / versionCode 14. Protocolo multiplayer 8: ambos os participantes devem atualizar.

## Revisão

Repouso e caminhada das 48 aparências usam medidas de apoio e altura por quadro, inclusive frente e costas. A direção visual tem uma margem nas diagonais para evitar alternância rápida entre vistas. Entradas menores que a zona morta não deslocam o personagem. As hitboxes não dependem do desenho.

Vida em 25% ou menos destaca a barra e mostra um aviso junto ao personagem e uma borda suave. Um sinal sonoro espaçado respeita a configuração de som. O parceiro local também recebe um aviso junto ao personagem.

Ao terminar a onda, os cacos restantes são atraídos durante 0,9 segundo antes da loja. Dinheiro e experiência são creditados uma única vez, também para os dois jogadores no cooperativo. A passagem da onda 20 para a região Aero preserva esses valores.

Tiros e avisos de área usam a paleta do inimigo que os criou. Habilidades usam paletas das roupas. O fundo do menu tem movimento suave de nuvens, ilha, flores e luz da porta, com botões estáveis. Foram removidos o painel de check-in, o botão da Sala de Ensaio e o botão de tela cheia das configurações; F11 continua disponível.

Seis retratos dedicados em alta definição: Kira, Armadilha de Urso Reversa, Puck, Coraline, Pequeno Príncipe e Felix. **Leon, Marceline e Wirt permanecem pendentes por limite do ImageGen**, usando suas imagens anteriores. Veja [registro de arte](PROMPTS-v0.8.md).

## Verificações

| Suíte | Resultado |
|---|---:|
| Campanha completa | 301/301 |
| Expansão e preços | 156/156 |
| Compra e persistência de roupas | 154/154 |
| Armas, controles e habilidades | 238/238 |
| Equilíbrio, coleta e atlas | 4898/4898 |
| Cooperativo | 14/14 |
| Arena | 34/34 |
| Direções de animação | 768/768 |
| Coleção 0.7 e migração | 63/63 |
| Revisão 0.8 | 23/23 |
| Total | 6649/6649 |

Campanha simulada: 39.115 passos e 9.164 inimigos derrotados, chegando à vitória na onda 40. Os 57 segundos de execução sem renderização não representam FPS de um aparelho.

`revision8.gd` verifica ausência de movimento sem entrada, coleta visível e crédito único nas ondas 1/20/40, passagem 20→21, crédito para ambos no cooperativo, paleta dos ataques e resolução dos seis retratos.

`ui8.gd`: zero falhas. Duas instâncias locais com protocolo 8 receberam a skin Felix e as vistas frontal e traseira, sem erros nos logs.

Revisão visual no Godot: menu, configurações, retrato de Kira, alerta de vida e quadros de repouso/caminhada. Teste gráfico confirma movimento do cenário com o botão Jogar imóvel e ausência dos botões removidos.

Windows exportado e executado em modo headless por 120 quadros, sem erros. Android exportado como `com.depoisdosono.game`, versão 0.8, código 14. Assinatura APK v2/v3 e alinhamento de 16 KiB aprovados. Os índices JSON de retratos e animação estão incluídos nos pacotes.

## Limites

Testes automatizados de rede ocorrem entre duas instâncias no mesmo computador. Não substituem teste físico PC–Android, controle, rede móvel ou desempenho de um telefone. Sem Mac/Xcode e assinatura Apple, não há IPA. O Android continua sendo um APK de teste com a chave local já usada nas versões anteriores. Não há relay para conexão automática fora da rede local.

Downloads: [release v0.8](https://github.com/Emanuelwqwq/Depois-dos-sonhos/releases/tag/v0.8). Código-fonte completo em Projeto-v0.8.zip, sem ferramentas locais, chaves ou saves.
