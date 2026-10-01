# Depois do Sono 1.3 — duas regiões, duas atmosferas

## Aero
- Materiais exclusivos gerados com ImageGen: resina perolada, cerâmica azul, porcelanato claro e água turquesa. Não reutiliza o musgo nem o xadrez do jardim.
- Marcos próprios: fonte de globo, portal aquático, entrada de vidro e escultura de golfinhos. O jardim preserva portas isoladas, relógios e escadas surreais.
- Dicas de controles, projéteis hostis e contornos de ataques ganham contraste sobre o piso claro.

## Animações e armas
- Repouso mais lento para todos os protagonistas e suas roupas, inclusive frente e costas. Caminhada continua vinculada à distância percorrida; não foram alterados velocidade, alcance ou hitboxes.
- Removida a sobreposição de duas poses na troca entre repouso e caminhada, que duplicava orelhas e pés.
- Noé/Jotaro: novas folhas isoladas de caminhada frontal e traseira, com oito quadros por direção. O repouso de costas segura uma pose neutra; o repouso frontal mantém as expressões anteriores. Recortes e âncoras medidos na imagem real.
- Puck: corrigido o recorte das caudas na caminhada de costas, preservando a ilustração original.
- Quatro sequências novas de efeitos, com seis quadros cada: cortes, água, sombra e pétalas. Integração nos ataques existentes, respeitando o limite de efeitos visíveis.
- Bolhas, pérolas de água e esferas de sombra têm silhuetas próprias em jogo. Bumerangues giram mais devagar; serras mantêm rotação rápida. Mãos e socos recebem movimento de avanço e recuperação. A lanterna projeta um cone de luz, em vez de parecer um golpe de espada.
- Sombras de inimigos acompanham o porte da criatura; retirado o círculo permanente sobre o personagem.

## Validação
12.458 verificações na suíte completa, sem falhas. Após o último ajuste de recortes, repetidos os testes de animação e da revisão 1.3. Capturas das duas regiões, cena de combate Aero e prévia animada de personagens/efeitos inspecionadas no Godot.

Teste de carga nesta sessão, Intel UHD: 63 inimigos, 48 projéteis, mediana e p95 de 16,67 ms/quadro, p99 de 17,99 ms. Isso não garante o mesmo resultado em celulares ou em outras condições de uso.

As mudanças gerais de reprodução abrangem as roupas existentes; esta entrega não redesenha todas as 126 folhas nem cria habilidade/esquiva frontal e traseira para todas as skins. Essas ações continuam usando perfil. Retoques de efeitos embutidos em algumas folhas antigas permanecem registrados na revisão 1.1; a arte nova de efeitos é uma camada separada.

Android físico, controle físico e rede externa continuam sem teste nesta máquina. APK de teste com a chave local existente. iPhone continua exigindo ambiente Apple e assinatura.

## Arte e fontes
[Prompts completos, arquivos e ferramenta](PROMPTS-v1.3.md). PNGs incorporados ao projeto, sem edição destrutiva das versões anteriores. Projeto-fonte e prévia acompanham os instaladores.
