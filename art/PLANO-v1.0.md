# Versão 1.0 — execução progressiva

Solicitação: implementar as propostas de jogabilidade, animação, efeitos e eventos, incluindo poderes obtidos pela combinação de skin e equipamento. Estimativas relativas de tokens, não orçamento ou medição. Implementação da versão 1.0; publicação registrada no relatório de validação.

## 1. Menor custo — ressonâncias
- [x] Subaru + Mão Invisível: prender comuns por 0,6s e gerar um aperto próximo ao ativar Ponto de retorno, causando 40% do dano base escalado da arma.
- [x] Remover automaticamente o bônus ao trocar a arma ou roupa; preservar saves; excluir PVP.
- [x] Explicar bônus ativo na pausa.
- [x] Expandir combinações temáticas com habilidades distintas e indicação antes da compra.
- [x] Testar ativação independente no coop e exclusão do PVP.

## 2. Baixo a médio — armas e quatro sinergias
- [x] Bumerangue + espelho: projétil refletido com 35% do dano, mantendo alcance limitado.
- [x] Sino + gelo: três pulsos congelam comuns por 0,8s; chefes recebem apenas lentidão.
- [x] Lanterna + sombra: explosão a cada três disparos, com 40% do dano em 80 passos.
- [x] Margarida + Chá: acumula 5 de vida efetivamente regenerada e libera descarga de 50% do dano; carga limitada a uma descarga.
- [x] Diferenciar preparação, trajeto e impacto das armas sem aumentar partículas indiscriminadamente.

## 3. Médio — evolução e recompensas
- [x] Duas opções de evolução com comportamento distinto, comparação legível e escolha explícita.
- [x] Calibrar escolhas, experiência e preços sem inflar cacos ou apagar progresso.

## 4. Médio a alto — eventos
- [x] Portas de sonho: desafio opcional com recompensa e risco claros.
- [x] Defender uma lembrança durante a onda.
- [x] Perseguir uma criatura especial.
- [x] Névoa com sinalização e objetivo legível, respeitando acessibilidade.

## 5. Alto — bosses
- [x] Um chefe do jardim com preparação, ataques evitáveis e janelas de recuperação.
- [x] Um chefe Aero com mecânica distinta e cores aquáticas.
- [x] Escalar coop e validar ausência de bloqueios de onda.

## 6. Maior custo — animação e efeitos
- [x] Transições suaves repouso/caminhada/esquiva, sem deslizar os pés.
- [x] Antecipação, ação, impacto e recuperação sincronizados com combate.
- [x] Efeitos por arma: silhueta, trajetória, impacto e cores coerentes.
- [x] Usar ImageGen quando forem necessários novos quadros; não substituir arte aprovada por outro estilo.
- [x] Validar frente/costas/perfil, skins e orçamento de efeitos.

## 7. Entrega
- [x] Testes reproduzíveis de combate, progressão, compras, coop e controles.
- [x] Revisão visual PC/toque, incluindo descrições longas.
- [x] Registrar separadamente validação pendente em dispositivos físicos.
- [x] Exportar e publicar EXE, APK e fonte 1.0 somente após validação.

## Validação parcial — 27/09/2026
Registro histórico da primeira etapa: Testes: resonance10 (17), gameplay4 (238), coop6 (14), guest_collection (154): 423 verificações aprovadas. Essas validações foram ampliadas na entrega final; ver VALIDACAO-v1.0.md. Nenhum teste físico Android realizado nesta etapa.

## Escopo final e limites
Implementadas quatro ressonâncias de roupa, quatro combinações de equipamento e duas evoluções por arma. Eventos usam a arte existente para lembrança/mariposa/luzes; névoa decorativa local não oculta ataques. Animações refinadas por reprodução, distância e transição, preservando folhas aprovadas; novos desenhos foram necessários apenas para os três ícones, gerados com ImageGen. A validação de toque foi simulada em PC; testes físicos permanecem explicitamente pendentes.
