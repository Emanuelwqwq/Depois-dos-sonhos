# Revisão de animações — 1.1

Inspeção visual das 125 folhas, em 32 páginas de contato, abrangendo os 3.632 quadros ativos. Essa inspeção não equivale a garantir continuidade perfeita em toda combinação de movimento e combate.

## Corrigido
- Ataques redesenhados com ImageGen integrado para Semente Aero, água-viva Aero e Santo da Piscina. Cada quadro mantém o corpo inteiro.
- Recorte da esquiva da Íris com roupa de folhagem e dos sete desenhos de derrota do Pipo/Yuri.
- Derrota da Rubi/Natsuki deixa de reiniciar em pé. Removido retorno intermediário do Puck.
- Quadros contendo apenas projéteis foram substituídos por poses completas de recuperação do mesmo personagem: Rubi original, espelho e salva-vidas.
- Removido pedaço de outra pose na esquiva da Rubi/Marceline.
- Inimigos passam a ter relógios próprios de apresentação: ataques iniciam no primeiro quadro, reações ao dano não usam a idade do monstro e a preparação longa dos bosses não recebe tempo negativo.
- Inimigos parados usam repouso. As mudanças de apresentação não alteram hitboxes, dano ou invencibilidade.

## Arte produzida
Ferramenta: ImageGen integrado, com transparência. Arquivos incorporados em `assets/sprites`: `aero_enemy4_attack11.png`, `aero_enemy7_attack11.png`, `dream_enemy11_attack11.png`.

Prompts: criar uma faixa horizontal de seis poses completas do mesmo personagem da referência, preservando identidade, paleta, proporções e acabamento; preparar, concentrar, comprimir, liberar, recuar e recuperar; sem projéteis separados ou efeitos atravessando as células, fundo transparente. Para o Santo: levantar braços de água, reunir no peito, abrir braços, recuar e recuperar. Para a água-viva: preservar cúpula azul vítrea e tentáculos verdes.

## Pendências explícitas
- A nova folha de direções do Noé/Jotaro foi rejeitada por ainda encostar pés e orelhas entre linhas. Mantida a arte anterior. A tentativa seguinte foi bloqueada pelo limite do ImageGen em 27/09/2026; aguardar disponibilidade, sem substituir o estilo.
- Alguns efeitos desenhados nas folhas ainda cruzam as bordas dos quadros (incluindo habilidades de folhagem/água e alguns inimigos Aero). Os defeitos graves de corpo ausente foram corrigidos; esses retoques não estão concluídos.
- Ações de habilidade/esquiva continuam em perfil; frente e costas cobrem repouso e caminhada. Esta revisão não criou todas as ações em todas as direções.
- Validação em aparelho Android físico e avaliação subjetiva da fluidez pelo jogador continuam pendentes.

Prévia reproduzida no Godot: `build/Animacoes-v1.1.mp4`. Galeria de quadros: `build/animation-review11/`. Teste automatizado: `tests/animation11.gd`.

## Validação desta entrega
12.237 verificações passaram, incluindo 5.527 de animação e limites dos recortes. Windows exportado e APK com assinatura/alinhamento verificados. Na cena de carga com 63 inimigos, Intel UHD: mediana 16,67 ms, percentil 95 de 18,52 ms. Não é uma garantia para outros aparelhos.
