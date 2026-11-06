# Scavenger Hunt

**Categoria:** OSINT / WEB EXPLOITATION

**Autor:** madStacks

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/161?page=1&bookmarked=true&workspace=true), possui a seguinte descrição:

> There is some interesting information hidden around this site. Can you find it?

### Resolução

Ao iniciar a instância, que é gerada aleatoriamente toda vez que o desafio é iniciado, recebemos um link para acessar um site, cujo endereço também é gerado aleatoriamente.

`http://xebec.cylabacademy.net:39540/`

Ao acessar o link fornecido, nos deparamos com o seguinte site:

<img width="935" height="274" alt="image" src="https://github.com/user-attachments/assets/f8313241-e315-479e-9aed-b660df00b78a" />

<img width="933" height="334" alt="image" src="https://github.com/user-attachments/assets/fa1aca61-f646-4c5b-9719-950f490975ef" />

Com base na dica fornecida pelo desafio, que menciona as tecnologias `HTML`, `CSS` e `JS (JavaScript)` utilizadas para desenvolver o site, podemos entender que algumas informações podem estar escondidas no próprio código-fonte da página. Para encontrá-las, pressionamos a tecla `F12` e acessamos as ferramentas de desenvolvedor do navegador.

Na aba `HTML`, encontramos o seguinte comentário:

`<!-- Here's the first part of the flag: academy{t -->`

<img width="887" height="474" alt="image" src="https://github.com/user-attachments/assets/ad136eb9-cab9-4f89-960f-5663f9fcc289" />

Anotamos essa primeira parte da FLAG e seguimos para a área de `CSS` para procurar outras informações escondidas. Nela, encontramos mais um comentário contendo a segunda parte:

`/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */`

<img width="986" height="704" alt="image" src="https://github.com/user-attachments/assets/292e7c56-bcd5-484d-86c5-f8e8ba4e91fa" />

Agora, seguindo para a última parte inicialmente indicada, a de `JavaScript`, não encontramos diretamente a terceira parte da FLAG, mas sim um comentário com a seguinte mensagem:

`/* How can I keep Google from indexing my website? */`

`"Como posso impedir que o Google indexe meu site?"`

<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/a3d6f393-10e9-4d17-b376-7a8281f93038" />

Essa mensagem nos dá uma dica sobre o arquivo `robots.txt`. Ele é utilizado em sites para informar aos mecanismos de busca, como o Google, quais páginas ou diretórios podem ou não ser rastreados. Esse arquivo fica localizado, geralmente, na raiz do site e pode ser acessado adicionando `/robots.txt` ao endereço.

Seguindo essa dica, colocamos `/robots.txt` na URL do site e somos direcionados para uma página que contém a próxima parte da FLAG e mais um comentário:

`# Part 3: t_0f_pl4c`

`# I think this is an apache server... can you Access the next flag?`

`"Acho que isso é um servidor Apache... você consegue encontrar a próxima FLAG?"`

<img width="1007" height="250" alt="image" src="https://github.com/user-attachments/assets/f2dbe52f-a373-446e-9f50-117498f0761a" />

O comentário menciona um servidor Apache, que é um software utilizado para hospedar e disponibilizar sites na internet. Uma de suas funcionalidades é o uso do arquivo `.htaccess`, que permite configurar determinadas regras e comportamentos do servidor, como redirecionamentos, controle de acesso e outras configurações.

Como o desafio menciona diretamente esse servidor, podemos utilizar essa informação como uma nova pista. Adicionando `/.htaccess` à URL do site, somos direcionados para outra página, que apresenta a quarta parte da FLAG e um novo comentário:

`# Part 4: 3s_2_lO0k`

`# I love making websites on my Mac, I can Store a lot of information there.`

`"Eu amo criar sites no meu Mac, posso armazenar muitas informações nele."`

<img width="1030" height="195" alt="image" src="https://github.com/user-attachments/assets/e3a255b7-dd32-4046-b9fb-319c86c708a2" />

A nova mensagem menciona um Mac, fazendo referência ao sistema operacional macOS. Esse sistema utiliza arquivos chamados `.DS_Store`, que armazenam informações sobre a organização e a visualização de arquivos e pastas no Finder.

Esses arquivos podem acabar ficando disponíveis publicamente quando um site é hospedado sem a devida configuração, revelando informações sobre sua estrutura de diretórios e arquivos. Aproveitando essa dica, adicionamos `/.DS_Store` à URL do site e encontramos a última parte da FLAG:

`Congrats! You've completed the scavenger hunt! Part 5: _2b9c61f}`

<img width="993" height="205" alt="image" src="https://github.com/user-attachments/assets/755c63d3-88ff-4b1b-9f14-c59e24b3ab85" />

Juntando todas as partes encontradas ao longo do desafio, chegamos à resposta final:

`academy{th4ts_4_l0t_0f_pl4c3s_2_lo0k_2b9c61f}`

### Conclusão

Com a resolução desse desafio, foi possível compreender como informações aparentemente simples podem revelar dados importantes sobre a estrutura e a configuração de um site. Comentários no código-fonte, arquivos de configuração e arquivos auxiliares podem armazenar informações que não ficam visíveis durante a navegação comum.

Durante o desafio, utilizamos diferentes recursos, como a inspeção dos códigos HTML, CSS e JavaScript, além da consulta aos arquivos `robots.txt`, `.htaccess` e `.DS_Store`, para encontrar cada parte da FLAG.

Dessa forma, o desafio demonstrou a importância da análise de informações públicas disponíveis em um site e como pequenos detalhes podem ser utilizados para identificar possíveis informações expostas e concluir uma investigação OSINT.
