# Cebola Criptográfica

**Categoria:** Criptografia.

### Introdução

Esse CTF, presente na Escolinha CTF, nos fornece um arquivo que contém o seguinte conteúdo:

00110101 00110010 00100000 00110110 01100010 00100000 00110111 00111000 00100000 00110100 00110010 00100000 00110101 00110010 00100000 00110011 00110011 00100000 00110111 00110100 00100000 00110100 00110101 00100000 00110100 01100100 00100000 00110101 00111000 00100000 00110101 00111001 00100000 00110111 01100001 00100000 00110110 00110011 00100000 00110110 01100001 00100000 00110101 00110101 00100000 00110011 00110000 00100000 00110110 00110011 00100000 00110011 00110001 00100000 00110011 00111001 00100000 00110110 01100001 00100000 00110100 01100101 00100000 00110100 00110111 00100000 00110011 00110000 00100000 00110011 00110000 00100000 00110101 00110010 00100000 00110100 00110100 00100000 00110101 00110001 00100000 00110011 00110001 00100000 00110110 00110110 00100000 00110101 00110001 00100000 00110011 01100100 00100000 00110011 01100100

Com ela nós podemos perceber que provalvemente se trata de um cifra e com essa informação já podemos ir para a resolução.

### Resolução

Essa resolução será inteiramente feita no site [`Dcode`](https://www.dcode.fr/en). Como inicialmente não temos conhecimento de qual cifra esse padrão se trata, buscamos o `Cipher Identifier` para termos uma direção e darmos o primeiro passo. Ao inserir a cifra, o site Dcode nos sugere o `ASCII Code`.

<img width="789" height="389" alt="image" src="https://github.com/user-attachments/assets/83012da9-d260-49d2-a437-92c27a6cb4c6" />

Agora, colocando a mesma cifra no `ASCII Code`, ela nos dá a seguinte cifra:

<img width="783" height="403" alt="image" src="https://github.com/user-attachments/assets/ffc02aa1-7768-46f5-87bb-d089414c65e0" />

Realizando o mesmo processo com a nova cifra fornecida, recebemos mais uma:

<img width="785" height="460" alt="image" src="https://github.com/user-attachments/assets/0a2748bc-fad2-4680-8819-bcb7fc365085" />

Caso tentemos colocar essa nova cifra no `ASCII Code`, serão obtidos valores totalmente sem sentido. Então, com essa informação, retornamos para o `Cipher Identifier` e colocamos a cifra obtida anteriormente. Como sugestão, recebemos a `Base 64 Coding`.

<img width="790" height="387" alt="image" src="https://github.com/user-attachments/assets/d7f87451-80ba-4b1a-9cb1-5af4ba977a0e" />

Por fim, colocando a cifra que tínhamos recebido anteriormente na `Base 64 Coding`, recebemos a flag que estávamos procurando: `FLAG{D1v3r54s_c4m4D45}`.

<img width="790" height="546" alt="image" src="https://github.com/user-attachments/assets/502027e1-8fb2-4570-a607-fe68aa580d00" />

### Conclusão

Como o próprio nome da flag diz, esse desafio possui diversas camadas, indo e voltando nas etapas para encontrarmos a cifra cada vez mais "traduzida" até chegarmos à resposta completa. Ele nos mostra como devemos utilizar as importantes ferramentas que possuímos na web para encontrarmos a resposta desejada.
