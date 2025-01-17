# Buscante

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.0.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.


# Curiosidades do curso

Programação reativa é um termo amplo, que não está restrito a uma linguagem ou a um framework específicos e pode inclusive ser utilizada no front ou backend. A programação reativa pode ser considerada um paradigma de programação ou modelo de arquitetura que se refere basicamente à manipulação de um fluxo de dados (streams) ou eventos de forma assíncrona.

Assim, a programação reativa se faz necessária em aplicações que precisam lidar de forma assíncrona com dados, quando fazemos uma requisição à API, por exemplo, e precisamos esperar esse retorno e também em programas que precisam processar informações em tempo real.

Dessa forma, escrevemos código que possa “reagir” às mudanças que acontecem (como eventos de cliques, dados sendo buscados, etc). Para isso, podemos utilizar a biblioteca RxJS, criada para construção de programas assíncronos ou baseados em eventos, através de uma sequência de observables.

## Padrão de projeto smart 
    O padrão de projeto Smart Components (ou Componentes Inteligentes) é um conceito usado no desenvolvimento de aplicativos front-end, especialmente em frameworks como Angular e React. Esse padrão ajuda a organizar o código e a separar responsabilidades dentro da aplicação. Aqui estão alguns pontos chave sobre o padrão Smart Components:

###    O que são Smart Components?
    Responsabilidade: Smart Components, também conhecidos como "Container Components", são responsáveis por gerenciar o estado, manipular dados e fornecer lógica de negócios. Eles geralmente conectam-se aos serviços, gerenciam o estado da aplicação e cuidam da lógica para manipular dados.

    Dados e Estado: Esses componentes frequentemente recebem dados e callbacks através de props (em React) ou inputs (em Angular). Eles também podem buscar dados de APIs e passar esses dados para seus componentes filhos, conhecidos como "Dumb Components" ou "Presentational Components".

    Não Exibem UI: Embora possam ter alguma lógica para controlar a exibição, eles geralmente não contêm lógica específica de UI ou estilos, deixando isso para os componentes filhos.

    Reutilização: Smart Components são menos reutilizáveis porque são mais específicos para a lógica da aplicação. Em vez disso, seu papel principal é orquestrar como os dados e ações fluem através da aplicação.

    Como os Smart Components se comparam com os Dumb Components?
    Dumb Components (Componentes Apresentacionais): São focados na apresentação e recebem dados e callbacks através de props/inputs. Eles não possuem lógica de negócios e não estão preocupados com a manipulação de dados. Seu objetivo é simplesmente renderizar a UI.

    Smart Components: Gerenciam a lógica e o estado da aplicação, e podem usar Dumb Components para renderizar a UI com base no estado atual.

    Exemplo em Angular
    Suponha que você esteja construindo uma aplicação que exibe uma lista de usuários:

    Smart Component: UserListContainerComponent - Este componente gerencia a busca de dados dos usuários, manipula a lógica de filtragem e ordenação e passa os dados para o componente de apresentação.

    Dumb Component: UserListComponent - Este componente recebe a lista de usuários e a lógica de filtragem via inputs e apenas se preocupa em renderizar a lista.

###    Benefícios do Padrão Smart Components
    Separação de Preocupações: Melhora a organização do código e facilita a manutenção.
    Testabilidade: Facilita o teste de componentes ao separar a lógica da apresentação.
    Reusabilidade: Permite reutilizar componentes apresentacionais em diferentes contextos sem duplicação de lógica.
    Como Implementar
    Criar Smart Components: Concentre a lógica de negócios e manipulação de dados aqui.
    Criar Dumb Components: Fique com a responsabilidade apenas de renderizar a UI.
    Manter a Comunicação: Passe dados e callbacks de Smart Components para Dumb Components.
    Esse padrão pode ser adaptado conforme a necessidade específica da sua aplicação, mas seguir a ideia de separar lógica e apresentação ajuda a manter o código mais limpo e organizado.



## Tipagem de variavel 

Posso criar a variável declarando tipo, porem quando inicializo a variável com o valor, não e obrigatório realizar a tipagem.
Exemplo:

Com tipagem 
 campoBusca: string = '';
 
 Sem tipagem 
  campoBusca = '';

Nos dois exemplo será consigerado um campo string.

## eventBinding

Exemplo:
 (click) = "buscarLivros()"


## Documentação do RXjs

https://rxjs.dev/


## CallBack

Na programação, um callback é uma função que é passada como argumento para outra função e é executada após a conclusão de uma operação ou um evento específico. A ideia é que você “chama de volta” a função fornecida quando a operação ou evento que a função principal está realizando termina.

Aqui estão alguns pontos importantes sobre callbacks:

Assíncronos e Síncronos: Callbacks podem ser usados tanto em operações assíncronas (como requisições de rede ou temporizadores) quanto em operações síncronas (como manipulação de arrays).

Exemplo em JavaScript:

javascript
Copiar código

```
function fetchData(callback) {
    setTimeout(() => {
        // Simula uma operação assíncrona (como uma requisição de API)
        const data = "Dados recebidos";
        callback(data); // Chama a função de callback com os dados recebidos
    }, 1000);
}

function handleData(data) {
    console.log(data); // Processa os dados recebidos
}
```

fetchData(handleData); // Passa a função handleData como callback para fetchData
Evita Bloqueios: Em operações assíncronas, callbacks ajudam a evitar bloqueios no código, permitindo que o programa continue executando enquanto aguarda a conclusão de uma tarefa.

Uso em Eventos: Callbacks são amplamente usados em programação de eventos, como na manipulação de eventos em interfaces gráficas de usuário (GUIs).

Callback Hell: Quando callbacks são aninhados em várias camadas, o código pode se tornar difícil de ler e manter. Esse problema é conhecido como “callback hell” ou “pyramid of doom”. Promises e async/await são soluções para mitigar esse problema.

Se você estiver trabalhando com uma ling


## Quick type

Ferramenta para auxiiar a tranformar o retorno da API em interfaces typcript

https://quicktype.io/

## Manter um campo como opcional na interface
Exemplo: Adicionasse o sinal ? após a declaração da variável
title?: string;

## Pipes do Angular

Os pipes são usados para transformar dados na exibição. Eles permitem que você formate valores de maneira simples diretamente no template HTML. Por exemplo, você pode usar pipes para formatar datas, números, textos, entre outros.

Aqui estão alguns exemplos de pipes integrados do Angular:

DatePipe: Formata uma data.

html

    {{ today | date:'shortDate' }}

    CurrencyPipe: Formata um número como moeda.

html

    {{ price | currency:'USD' }}
    DecimalPipe: Formata números decimais.

html

    {{ number | number:'1.2-2' }}
    PercentPipe: Formata um número como percentual.

html

    {{ percentage | percent }}

Você também pode criar seus próprios pipes personalizados para atender às necessidades específicas do seu aplicativo. Para criar um pipe personalizado, você deve definir uma classe com o decorador @Pipe e implementar o método transform. Aqui está um exemplo básico:

typescript

```
    import { Pipe, PipeTransform } from '@angular/core';

    @Pipe({
    name: 'reverse'
    })
    export class ReversePipe implements PipeTransform {
    transform(value: string): string {
        return value.split('').reverse().join('');
    }
    }
```

#### Você tambem pode criar um novo pipe utilizando a linha de comando
#### ng g pipe pipes/autoria

Então, você pode usar esse pipe em seu template:

html

    {{ 'Hello' | reverse }} <!-- Output: 'olleH' -->

Os pipes são uma maneira poderosa de manipular e formatar dados de forma declarativa em seus templates Angular.



## Typewriter Header
O Typewriter Header é uma técnica de design onde o texto parece ser digitado em tempo real, criando um efeito de digitação. Esse efeito pode ser usado para dar uma sensação dinâmica e interativa ao seu site ou aplicação.


## Buscar dinâmica com keyUP

No Angular, o evento keyup é um evento nativo do DOM que é acionado quando uma tecla é liberada (ou seja, quando o usuário solta uma tecla após pressioná-la). Em Angular, você pode usar esse evento para executar uma função sempre que uma tecla é pressionada e liberada.

Exemplo (keyup)="buscarLivros()"

## Convensão para declarar variaveis do tipo observabo deve utilizar o $
exemplo:
 livrosEncontrados$


## SwitchMap

No Angular, o operador switchMap é uma ferramenta poderosa da biblioteca RxJS, usada para manipulação e transformação de fluxos de dados em Observables. Ele é especialmente útil para cenários em que você precisa cancelar operações anteriores quando uma nova operação é emitida, como em buscas em tempo real ou quando uma ação do usuário dispara uma série de eventos.

O que é switchMap?
switchMap é um operador que mapeia um Observable para outro Observable e emite os valores desse novo Observable. Se um novo valor for emitido pelo Observable de origem antes que o Observable interno tenha completado, switchMap cancela a assinatura do Observable interno anterior e se inscreve no novo Observable.

Isso é útil em cenários como pesquisas em tempo real, onde você quer garantir que apenas a pesquisa mais recente seja considerada, ignorando resultados de pesquisas anteriores.


## Operadores RxJS

switchMap - Operador de Transformação. Cancela requisições de observables anteriores, emitindo valores apenas do Observable projetado mais recentemente.

filter - Operador de filtragem. Filtra os itens emitidos pelo Observable de origem, permitindo apenas aqueles que satisfaçam uma condição especificada.

debounceTime - Operador de filtragem. Retorna um Observable que atrasa as emissões do Observable de origem pelo tempo especificado.

distinctUntilChanged - Operador de filtragem. Retorna um Observable que emite todos os valores enviados pelo observable de origem se forem distintos em comparação com o último valor emitido pelo observable de resultado.