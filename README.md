# Agendamento de Evento

Este projeto é um formulário de agendamento de eventos desenvolvido em Flutter. A tela permite escolher a data, o horário, o tipo de evento, a quantidade de convidados, a visibilidade, os serviços adicionais e possíveis restrições alimentares.

## Resumo do Desenvolvimento


### 1. Qual o nome do componente Slider? Qual a variável responsável por armazenar o
valor padrão do Slider?


O componente usado é o `Slider`. Ele permite escolher um valor dentro de um intervalo deslizando o controle na tela.A variável `_quantidadeConvidados` guarda a quantidade de convidados escolhida.

### 2. Porque em um dos botões um está marcado como “OutlinedButton” e o outro como “ElevatedButton”? Qual a diferença visual entre eles? Possuem parâmetros diferentes? Quais?

O botão Cancelar usa `OutlinedButton` porque tem apenas uma borda e um fundo transparente, ficando visualmente mais discreto. Já o botão Salvar usa `ElevatedButton`, que possui fundo preenchido e maior destaque visual.

Eles também podem receber estilos diferentes por meio do parâmetro `style`. No projeto, o botão Cancelar usa borda e texto vermelhos, enquanto o botão Salvar usa a cor principal do tema.

### 3. Qual a finalidade do método setState() dentro do RadioGroup?

O `setState()` informa ao Flutter que o valor selecionado mudou e que a tela precisa ser reconstruída. Assim, quando o usuário escolhe uma opção de visibilidade, como Público, Privado ou Apenas Convidados, `_visibilidadeSelecionada` é atualizado e o rádio escolhido aparece marcado corretamente.

### 4. Explique para uma criança de 10 anos o que faz o método “.map” na lista de itens do dropdown.

Imagine que você tem uma caixa com vários cartões escritos: “Aniversário”, “Casamento”, “Corporativo” e “Outro”. O `.map()` pega um cartão de cada vez e coloca cada nome dentro de uma opção que o menu consegue entender.

Por exemplo, ele faz algo parecido com isto:

1. Pega “Aniversário” e cria uma opção do menu.
2. Pega “Casamento” e cria outra opção.
3. Pega “Corporativo” e cria mais uma opção.
4. Pega “Outro” e cria a última opção.

Depois, o dropdown junta todas essas opções e mostra uma lista para o usuário escolher. Então, o `.map()` funciona como uma pessoa que transforma vários cartões simples em várias opções organizadas dentro de um menu. Ele não escolhe uma opção sozinho; apenas prepara todas elas para aparecerem na tela.

### 5. Como é controlado as tags selecionadas do usuário do tipo Chip (FilterChip)?


As tags escolhidas ficam guardadas na lista `_tagsSelecionadas`. Quando o usuário seleciona uma tag, ela é adicionada à lista. Quando desmarca, ela é removida. O `FilterChip` usa essa lista para saber quais tags devem aparecer selecionadas na tela.
