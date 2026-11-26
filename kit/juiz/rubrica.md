# Rubrica — mensagem de commit escrita pelo agente

Critérios sim/nêo. Nunca nota de 1 a 10. (invariável) = um "nao" reprova a mensagem, independente do resto.
O que dá para checar por código (tamanho da 1ª linha, formato) NêO entra aqui: vai para um teste.

R1 | A mensagem diz POR QUE a mudança foi feita, nêo só o que mudou? | qualidade
R2 | Toda MUDANÇA que a mensagem cita está no diff (nêo inventa arquivo, teste nem efeito)? O motivo pode vir de fora do diff. | invariável
R3 | Quem nêo viu o diff entende o que mudou só pela mensagem? | qualidade
