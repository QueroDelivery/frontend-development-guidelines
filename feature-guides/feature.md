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


