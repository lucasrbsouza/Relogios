# "Relogios

## Relógio Digital e Analógico

Este é um script JavaScript para um relógio digital. Ele exibe a hora atual em formato digital e também move os ponteiros de um relógio analógico para representar a hora atual.

### Como usar

1. Primeiro, você precisa ter três elementos em seu HTML com as classes `.digital`, `.p_s`, `.p_m` e `.p_h`. O elemento com a classe `.digital` será usado para exibir a hora digital, enquanto os elementos com as classes `.p_s`, `.p_m` e `.p_h` serão usados para os ponteiros de segundos, minutos e horas do relógio analógico, respectivamente.

2. Em seguida, inclua o script em seu arquivo HTML.

### Detalhes do Código

O código começa selecionando os elementos necessários do DOM usando `document.querySelector`.

A função `updateClock` é chamada a cada segundo usando `setInterval(updateClock, 1000)`. Esta função faz o seguinte:

- Obtém a hora atual usando `new Date()`.
- Extrai as horas, minutos e segundos da hora atual.
- Atualiza o elemento digital com a hora atual formatada.
- Calcula os graus de rotação para cada ponteiro do relógio analógico com base na hora atual.
- Atualiza a transformação de rotação de cada ponteiro do relógio analógico.

A função `fixZero` é usada para adicionar um zero à esquerda aos números de um dígito, garantindo que sempre haja dois dígitos exibidos para horas, minutos e segundos.

Por fim, `updateClock` é chamado uma vez no início para garantir que o relógio seja exibido imediatamente quando a página for carregada, em vez de esperar um segundo para a primeira chamada de `setInterval`.
