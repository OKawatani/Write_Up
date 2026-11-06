# Cookies

**Categoria:** Web

**Autor:** madStacks

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/173?page=1&bookmarked=true&workspace=true), possui a seguinte descrição:

> Who doesn't love cookies? Try to figure out the best one.

### Resolução

Ao iniciar a instância, que é gerada aleatoriamente toda vez que o desafio é iniciado, recebemos um link para acessar um site, cujo endereço também é gerado aleatoriamente.

`http://chatelaine.cylabacademy.net:10166/`

Ao acessar o link fornecido, nos deparamos com o seguinte site:

<img width="959" height="569" alt="image" src="https://github.com/user-attachments/assets/9e24e20a-ad05-44d5-8cf5-f7862ad039a1" />

Como o desafio é baseado em cookies, o primeiro lugar que procurei foi a aba de armazenamento de cookies do navegador, acessada por meio da tecla F12, nas ferramentas de desenvolvedor.

<img width="1919" height="914" alt="image" src="https://github.com/user-attachments/assets/46698ae9-8870-4142-831e-e9b597fa6044" />

Nessa aba, encontramos uma variável chamada `name`, cujo valor (`value`) era `-1`. Ao alterar o valor dessa variável para `1` e atualizar a página, o conteúdo do menu muda para `I love chocolate chips cookies!`.

<img width="700" height="369" alt="image" src="https://github.com/user-attachments/assets/4ff76b50-cd65-4440-9d41-6689c6b23eed" />

Testando diferentes valores nessa variável, percebemos que as respostas do site mudavam de acordo com o número informado, apresentando diferentes tipos de cookies. Após continuar os testes, ao inserir o número `18` no campo `value`, uma resposta diferente apareceu, revelando a FLAG do desafio:

`academy{3v3ry1_l0v3s_c00k135_90a3a7cb}`

<img width="1919" height="343" alt="image" src="https://github.com/user-attachments/assets/8558f8e6-d623-4052-bf69-d3dea57d51dd" />

### Conclusão

Com a resolução desse desafio, foi possível compreender como os cookies podem armazenar informações utilizadas por um site para controlar seu comportamento e apresentar conteúdos diferentes ao usuário.

Ao inspecionar os cookies por meio das ferramentas de desenvolvedor do navegador, conseguimos identificar a variável responsável pela alteração das respostas do site. Modificando seu valor e testando diferentes possibilidades, encontramos a combinação que revelou a FLAG necessária para concluir o desafio.
