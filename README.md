# Boas vindas ao repositório do projeto de testes com a React Testing Library!

Você já usa o GitHub diariamente para desenvolver os exercícios, certo? Agora, para desenvolver os projetos, você deverá seguir as instruções a seguir. Fique atento a cada passo, e se tiver qualquer dúvida, nos envie por _Slack_! #vqv 🚀

Aqui você vai encontrar os detalhes de como estruturar o desenvolvimento do seu projeto a partir deste repositório, utilizando uma branch específica e um _Pull Request_ para colocar seus códigos.

## Neste projeto, verificamos se você é capaz de:

1. Realizar testes automatizados das suas aplicações em React usando o `Jest` e o `React Testing Library` (RTL)

## O que deverá ser desenvolvido

Nesse projeto você escreverá testes para uma aplicação React.

## Desenvolvimento

Este repositório já contém uma aplicação React criada e configurada. Após clonar o projeto e instalar as dependências (mais sobre isso abaixo), você não precisará realizar nenhuma configuração adicional. Você deverá utilizar [`Jest`](https://jestjs.io/) e a biblioteca [`React Testing Library`](https://testing-library.com/) (também já instaladas e configuradas) para escrever os testes. Note que a aplicação contém uma implementação completa de todos os requisitos da Pokédex. Seu trabalho será, para cada requisito listado a seguir, escrever testes que garantam sua corretude. Cuidado com [testes _falsos positivos_](https://talkingabouttesting.com/2015/08/04/falsos-negativos-falsos-positivos-verdadeiros-negativos-e-verdadeiros-positivos/). Falsos positivos serão desconsiderados na avaliação.

### Quem testa os testes?

  Nesse trabalho o avaliador automatizado **testam os testes de vocês!** A ideia dele é a seguinte: você vai escrever casos de teste para a aplicação, certo? E esses testes têm que garantir que a aplicação está funcionando, certo? Pois bem! Se eu quebro uma parte da aplicação, fazendo uma alteração no código, seus testes devem quebrar, certo? Pois é isso que o avaliador faz.
  Como assim? Pense da seguinte forma: nosso avaliador vai navegar por toda a aplicação da Pokédex e vai fazer várias mudanças no código dela **para que ela quebre e pare de funcionar**. Em seguida ele vai rodar seus testes. Caso seus testes não acusem que aplicação está com problemas o avaliador não vai aprovar aquele requisito! Se, para todas as alterações que o avaliador fizer no código da aplicação, os seus testes acusarem problemas, tudo será aprovado! O avaliador garante, portanto, que seus testes testam a aplicação da Pokédex como se deve!
  Na linguagem do avaliador, dizemos que cada mudança que o avaliador faz na sua aplicação é um **mutante**. O avaliador cria vários mutantes e seus testes **devem matar todos!** Se algum mutante sobreviver, temos problemas. Certo? Vamos aos requisitos então!

## Requisitos do projeto

A seguir estão listados todos os requisitos do projeto. Lembre-se que para a avaliação utilizaremos testes por mutação, então cada requisito só será aceito se os testes tiverem comportamento adequado tanto na aplicação original como na modificada.

Todos os arquivos de teste que vocês usarão **já estão previamente criados e novos arquivos não devem ser criados**. Como exemplo colocamos um teste dentro do arquivo `src/tests/App.test.js`. Além disso, **cada requisito se refere a um arquivo da aplicação da Pokédex**. Obter aprovação num requisito significa que todos os casos de erro daquele arquivo estão cobertos, ou seja, todos os mutantes criados naquele arquivo pelo avaliador foram mortos. Nos subitens de cada requisito detalhamos o que é necessário fazer para obter a aprovação neles.

### 1. Testando o arquivo App.js

  - Teste se a página principal da Pokédex é renderizada ao carregar a aplicação no caminho de URL `/`.

  - Teste se o topo da aplicação contém um conjunto fixo de links de navegação

    - Verifique se o primeiro link possui o texto `Home` com a URL `/`;

    - Verifique se o segundo link possui o texto `About` com a URL `/about`;

    - Verifique se o terceiro link possui o texto `Favorite Pokémons` com a URL `/favorites`.

  - Teste se a aplicação é redirecionada para a página inicial, na URL `/` ao clicar no link `Home` da barra de navegação. 

  - Teste se a aplicação é redirecionada para a página de `About`, na URL `/about`, ao clicar no link `About` da barra de navegação. 

  - Teste se a aplicação é redirecionada para a página de `Pokémons Favoritados`, na URL `/favorites`, ao clicar no link `Favorite Pokémons` da barra de navegação.

  - Teste se a aplicação é redirecionada para a página `Not Found` ao entrar em uma URL desconhecida.

### 2. Testando o arquivo About.js

  - Teste se a página contém as informações sobre a Pokédex.

  - Teste se a página contém um heading `h2` com o texto `About Pokédex`;

  - Teste se a página contém dois parágrafos com texto sobre a Pokédex;

  - Teste se a página contém a seguinte imagem de uma Pokédex: `https://cdn.bulbagarden.net/upload/thumb/8/86/Gen_I_Pok%C3%A9dex.png/800px-Gen_I_Pok%C3%A9dex.png`.

### 3. Testando o arquivo FavoritePokemons.js

  - Teste se é exibido na tela a mensagem `No favorite pokemon found`, caso a pessoa não tenha pokémons favoritos.

  - Teste se é exibido todos os cards de pokémons favoritados.

  - Teste se **Não** é exibido nenhum card de pokémon não favoritado.

### 4. Testando o arquivo NotFound.js

  - Teste se página contém um heading `h2` com o texto `Page requested not found 😭`;

  - Teste se página mostra a imagem `https://media.giphy.com/media/kNSeTs31XBZ3G/giphy.gif`.

### 5. Testando o arquivo Pokedex.js

  - Teste se é exibido o próximo Pokémon da lista quando o botão `Próximo pokémon` é clicado.

    - Verifique se o botão contém o texto `Próximo pokémon`;

    - Verifique se os próximos Pokémons da lista são mostrados, um a um, ao clicar sucessivamente no botão.

    - Verifique se o primeiro Pokémon da lista é mostrado ao clicar no botão se estiver no último Pokémon da lista.

  - Teste se é mostrado apenas um Pokémon por vez.

  - Teste se a Pokédex tem os botões de filtro

    - Verifique se somente os Pokémons do tipo selecionado através do `botão de tipo` estão circulados.

    - Verifique se o texto do botão é o `nome do tipo`, ex. `Psychic`.

  - Teste se a Pokédex contém um botão para resetar o filtro

    - Verifique se o texto do botão é `All`.

    - Verifique se a Pokedéx volta a circular por todos os Pokémons quando o botão for clicado.

    - Verifique se, ao carregar a página, o filtro selecionado seja `All`.

  - Teste se é criado, dinamicamente, um botão de filtro para cada tipo de Pokémon.

    - Verifique se os botões de filtragem estão dinâmicos.

    - Verifique se existe um botão de filtragem para cada tipo de Pokémon disponível nos dados, independente de quais ou quantos sejam, sem repetição de tipos. Ou seja, confira se a sua Pokédex possui pokémons do tipo `Fire`, `Psychic`, `Electric` e `Normal`.
    
    - Verifique se é mostrado como opção de filtro um botão para cada um dos tipos. Além disso, o botão `All` deve estar sempre visível.

  - Teste se o botão de `Próximo pokémon` está desabilitado quando a lista filtrada de Pokémons tiver apenas um pokémon.

### 6. Testando o arquivo Pokemon.js

  - Teste se é msotrado um card com as informações de determinado pokémon.

  - Teste se o nome correto do Pokémon é mostrado na tela.

  - Teste se o peso médio do pokémon é exibido com um texto no formato `Average weight: <value> <measurementUnit>`; onde `<value>` e `<measurementUnit>` são, respectivamente, o peso médio do pokémon e sua unidade de medida.

  - Teste se a imagem do Pokémon é exibida. Ela deve conter um atributo `src` com a URL da imagem e um atributo `alt` com o texto `<name> sprite`, onde `<name>` é o nome do pokémon.

  - Teste se o card do Pokémon indicado na Pokédex contém um link de navegação para exibir detalhes deste Pokémon. O link deve possuir a URL `/pokemons/<id>`, onde `<id>` é o id do Pokémon exibido;

  - Teste se ao clicar no link de navegação do Pokémon, é feito o redirecionamento da aplicação para a página de detalhes de Pokémon. 
  
  - Teste também se a URL exibida no navegador muda para `/pokemon/<id>`, onde `<id>` é o id do Pokémon cujos detalhes se deseja ver;

  - Teste se existe um ícone de estrela nos Pokémons favoritados.

    - Verifique se o ícone é uma imagem com o atributo `src` contendo o caminho `/star-icon.svg`;

    - Verifique se a imagem tem o atributo `alt` igual a `<pokemon> is marked as favorite`, onde `<pokemon>` é o nome do Pokémon exibido.

### Testando o arquivo PokemonDetails.js

  - Teste se as informações detalhadas do Pokémon selecionado são mostradas na tela.

  - Teste se a página contém um texto `<name> Details`, onde `<name>` é o nome do Pokémon;

  - Teste se **Não** há o link de navegação para os detalhes do Pokémon selecionado.

  - Teste se a seção de detalhes contém um heading `h2` com o texto `Summary`.

  - Teste se a seção de detalhes contém um parágrafo com o resumo do Pokémon específico sendo visualizado.

  - Teste se existe na página uma seção com os mapas contendo as localizações do pokémon

    - Verifique se contém, na seção de detalhes, um heading `h2` com o texto `Game Locations of <name>`; onde `<name>` é o nome do Pokémon exibido.

    - Verifique se todas as localizações do Pokémon são mostradas na seção de detalhes;

    - Verifique se são exibidos o nome da localização e uma imagem do mapa em cada localização.

    - Verifique se a imagem da localização tem um atributo `src` com a URL da localização.

    - Verifique se a imagem a imagem da localização tem um atributo `alt` com o texto `<name> location`, onde `<name>` é o nome do Pokémon.

  - Teste se o usuário pode favoritar um pokémon através da página de detalhes

    - Verifique se a página exibe um checkbox que permite favoritar o Pokémon.
    - Verifique se os cliques alternados no checkbox adicionam e removem o Pokémon da lista de favoritos.

    - Verifique se o label do checkbox é `Pokémon favoritado?`.

## Quer fazer mais? Temos algumas sugestões!

O que temos a seguir não são requisitos bônus - são ideias para você se aprofundar mais no projeto e **aprender mais!** Que tal trabalhar neles? Começamos com algo bem direto:

  - A cobertura de testes deve ser 100%

    - Para ver a cobertura de testes, execute no terminal o comando `npm run test-coverage`.

Além disso, a Pokédex é uma aplicação estática, com seus dados pré-definidos. Utilizando a [PokéAPI](https://pokeapi.co/), é possível deixá-la mais dinâmica e realista.

Se quiser implemente os requisitos propostos a seguir e escreva testes para eles. Tente manter sempre a cobertura de testes em 100%, garantindo assim que não há código ou fluxos lógicos não testados. Para um desafio adicional, tente utilizar TDD - escreva os testes à medida que for implementando os requisitos.

  - Adicione uma rota para exibir uma lista de localizações

    - A URL da rota deve ser `/locations`;

    - A página deve exibir uma lista com as localizações retornadas pela PokéAPI. Você pode ler [aqui](https://pokeapi.co/docs/v2.html/#resource-lists-section) e [aqui](https://pokeapi.co/docs/v2.html/#locations-section) como utilizar a PokéAPI para buscar uma lista de localizações.

  - Adicione na barra de navegação um link para a lista de localizações

    - O link deve conter o texto `Locations`;

    - Ao clicar no link, a página com a lista de localizações deve ser exibida.

  - Adicione botões de paginação na lista de localizações

  Por default, os _endpoints_ da PokéAPI retornam no máximo 20 resultados. Utilizando os parâmetros `limit` e `offset`, você pode especificar qual página deseja buscar e qual seu tamanho. Veja [aqui](https://pokeapi.co/docs/v2.html/#resource-lists-section) como utilizar estes parâmetros.

    - Adicone dois botões "Anterior" e "Próxima" que permitam navegar entre as página da lista de localizações;

    - Na primeira página, o botão "Anterior" deve ser desabilitado. Da mesma forma, ao alcançar a última página, o botão "Próximo" deve ser desabilitado.

  - Adiciona uma rota para exibir uma lista de gerações

    - A URL da rota deve ser `/generations`;

    - A página deve exibir uma lista com as gerações retornadas pela PokéAPI. Você pode ler [aqui](https://pokeapi.co/docs/v2.html/#resource-lists-section) e [aqui](https://pokeapi.co/docs/v2.html/#generations) como utilizar a PokéAPI para buscar uma lista de gerações.

  - Adicione na barra de navegação um link para a lista de gerações

    - O link deve conter o texto `Generations`;

    - Ao clicar no link, a página com a lista de gerações deve ser exibida.

  - Adicione uma rota para exibir informações sobre uma geração

    - A URL da rota deve ser `/generations/<id>`, onde `<id>` é o id da geração exibida;

    - A página deve exibir, após buscar na PokéAPI, o nome da geração e uma lista com os nomes dos pokémons introduzidos nesta geração.

  - Adicione a cada geração na lista de gerações um link para a página de detalhes desta geração

    - Ao clicar no link, a página com informações sobre a geração clicada deve ser exibida.

---

## Instruções para entregar seu projeto:

### ANTES DE COMEÇAR A DESENVOLVER:

1. Clone o repositório
  * `git clone git@github.com:tryber/sd-0x-block16-project-react-testing-library.git`.
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd sd-0x-block16-project-react-testing-library`

2. Instale as dependências
  * `npm install`

3. Crie uma branch a partir da branch `master`
  * Verifique que você está na branch `master`
    * Exemplo: `git branch`
  * Se não estiver, mude para a branch `master`
    * Exemplo: `git checkout master`
  * Agora crie uma branch para qual você vai submeter os `commits` do seu projeto
    * Você deve criar uma branch no seguinte formato: `nome-de-usuario-nome-do-projeto`
    * Exemplo: `git checkout -b joaozinho-react-testing`

4. Adicione um teste para algum dos requisitos do projeto. Por exemplo, para o requisito #1, adicione em `App.test.js`:

```javascript
test('shows the Pokédex when the route is `/`', () => {
  const { getByText } = render(
    <MemoryRouter initialEntries={['/']}>
      <App />
    </MemoryRouter>,
  );

  expect(getByText('Encountered pokémons')).toBeInTheDocument();
});
```

5. Adicione as mudanças ao _stage_ do Git e faça um `commit`
  * Verifique que as mudanças ainda não estão no _stage_
    * Exemplo: `git status` (deve aparecer listado o arquivo _src/last.js_ em vermelho)
  * Adicione o arquivo alterado ao _stage_ do Git
      * Exemplo:
        * `git add .` (adicionando todas as mudanças - _que estavam em vermelho_ - ao stage do Git)
        * `git status` (deve aparecer listado o arquivo _src/last.js_ em verde)
  * Faça o `commit` inicial
      * Exemplo:
        * `git commit -m 'iniciando o projeto. VAMOS COM TUDO :rocket:'` (fazendo o primeiro commit)
        * `git status` (deve aparecer uma mensagem tipo _nothing to commit_ )

6. Adicione a sua branch com o novo `commit` ao repositório remoto
  * Usando o exemplo anterior: `git push -u origin joaozinho-react-testing`

7. Crie um novo `Pull Request` _(PR)_
  * Vá até a página de _Pull Requests_ do [repositório no GitHub](https://github.com/tryber/sd-0x-block16-project-react-testing-library/pulls)
  * Clique no botão verde _"New pull request"_
  * Clique na caixa de seleção _"Compare"_ e escolha a sua branch **com atenção**
  * Clique no botão verde _"Create pull request"_
  * Adicione uma descrição para o _Pull Request_ e clique no botão verde _"Create pull request"_
  * **Não se preocupe em preencher mais nada por enquanto!**
  * Volte até a [página de _Pull Requests_ do repositório](https://github.com/tryber/sd-0x-block16-project-react-testing-library/pulls) e confira que o seu _Pull Request_ está criado

---

### DURANTE O DESENVOLVIMENTO

* Faça `commits` das alterações que você fizer no código regularmente

* Lembre-se de sempre após um (ou alguns) `commits` atualizar o repositório remoto

* Os comandos que você utilizará com mais frequência são:
  1. `git status` _(para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage)_
  2. `git add` _(para adicionar arquivos ao stage do Git)_
  3. `git commit` _(para criar um commit com os arquivos que estão no stage do Git)_
  4. `git push -u nome-da-branch` _(para enviar o commit para o repositório remoto na primeira vez que fizer o `push` de uma nova branch)_
  5. `git push` _(para enviar o commit para o repositório remoto após o passo anterior)_

---

### DEPOIS DE TERMINAR O DESENVOLVIMENTO (OPCIONAL)

Para **"entregar"** seu projeto, siga os passos a seguir:

* Vá até a página **DO SEU** _Pull Request_, adicione a label de _"code-review"_ e marque seus colegas
  * No menu à direita, clique no _link_ **"Labels"** e escolha a _label_ **code-review**
  * No menu à direita, clique no _link_ **"Assignees"** e escolha **o seu usuário**
  * No menu à direita, clique no _link_ **"Reviewers"** e digite `students`, selecione o time `tryber/students-sd-0x`

Se ainda houver alguma dúvida sobre como entregar seu projeto, [aqui tem um video explicativo](https://vimeo.com/362189205).

---

### REVISANDO UM PULL REQUEST

⚠⚠⚠

À medida que você e os outros alunos forem entregando os projetos, vocês serão alertados **via Slack** para também fazer a revisão dos _Pull Requests_ dos seus colegas. Fiquem atentos às mensagens do _"Pull Reminders"_ no _Slack_!

Os monitores também farão a revisão de todos os projetos, e irão avaliar tanto o seu _Pull Request_, quanto as revisões que você fizer nos _Pull Requests_ dos seus colegas!!!

Use o material que você já viu sobre [Code Review](https://course.betrybe.com/real-life-engineer/code-review/) para te ajudar a revisar os projetos que chegaram para você.
