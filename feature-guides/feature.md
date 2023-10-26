## Característica

Às vezes, será difícil decidir o que é uma feature e o que não é.
### O problema é o núcleo

No centro de qualquer feature, há um problema. Um problema é uma razão pela qual você tem uma feature em primeiro lugar. O primeiro passo para identificar o nome e o escopo da feature é definir qual problema ele deve resolver.

Uma vez que a definição do problema esteja claramente definida, é provável que seja fácil dizer qual feature você está construindo e o que ele deve ou não fazer.

### Exemplo de login

Por exemplo, digamos que queremos implementar uma funcionalidade de login.

A primeira coisa que precisamos entender é por que precisamos de um login em primeiro lugar e o que é. Em termos simples, o login é uma maneira de identificar um usuário. Login tem um botão de login e logout, um formulário de login, formulário de login esquecido e potencialmente outras funções.

Generalizado, o login é uma forma de autenticação. O problema que ele resolve é a necessidade de fornecer acesso a determinados dados apenas para usuários autenticados.

Portanto, poderíamos chamar a feature de "autenticação" e o botão de login, e o formulário de login são seus detalhes de implementação.

Tendo a definição do feature como "autenticação", poderíamos adicionar autenticação usando um serviço OAuth. Ainda faria parte da feature de "autenticação" porque está resolvendo o mesmo problema.

## Feature === Domínio

A utilização do conceito de domínio em aplicações frontend é uma maneira eficiente de agrupar diversas micro funcionalidades em grupos que compartilham o mesmo contexto.

Imagine que você está desenvolvendo um aplicativo de comércio eletrônico. Este aplicativo pode abranger diversos domínios(features), como Usuários, Produtos, Pedidos, Pagamentos, entre outros. Cada um desses domínios possui suas próprias responsabilidades e regras de negócios.

No DDD (Domain-Driven Design), um domínio representa um contexto de conhecimento ou atividades. No nosso caso, o domínio irá representar um conjunto de funcionalidades que compartilham do mesmo contexto.
Cada domínio deve ser independente e não deve depender de outro domínio. Isso quer dizer que se você está trabalhando no domínio “Pedidos”, ele não deve estar diretamente ligado aos domínios de “Produtos” ou “Usuários”, por exemplo. Isso mantém a separação de preocupações e torna o código mais gerenciável.

Contudo, na prática, é possível que haja situações em que um domínio necessite de outro domínio. A solução mais adequada para este caso seria criar uma interface ou serviço capaz de fornecer os dados necessários sem revelar os dados internos do outro domínio. Esse princípio é conhecido como princípio da inversão de dependência. Se uma funcionalidade precisar de algo que exista em outro domínio, considere criar um serviço compartilhado ou utilitário que possa ser usado por diversos domínios. Se estiver representando um mesmo objeto em domínios distintos, como um pedido(por exemplo), o ideal é que recrie a interface de acordo com as necessidades do domínio em que está sendo utilizada.
