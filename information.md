# Information

**Categoria:** Forense

**Autor:** susie

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/186?page=1&search=informa&workspace=true), possui a seguinte descrição, acompanhada de um arquivo `.jpg`:

> Files can always be changed in a secret way. Can you find the flag? cat.jpg

<img width="1054" height="656" alt="image" src="https://github.com/user-attachments/assets/b3058afa-c14d-4d7f-8c2f-c44c5dd5eef7" />

### Desenvolvimento

Por se tratar de um arquivo JPG e considerando a descrição, que diz que arquivos podem ser alterados de uma forma secreta, podemos entender que o desafio está relacionado aos metadados da imagem.

Para verificar essas informações, utilizei o site [Exif.tools](https://exif.tools/), que permite visualizar os metadados de arquivos de imagem e identificar possíveis informações escondidas.

<img width="888" height="880" alt="image" src="https://github.com/user-attachments/assets/1eb044c2-678f-4f74-8ca5-fea331ff42d2" />

Analisando a seção `License / Resource`, identificamos um valor incomum: `YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9`.

Para descobrir o que esse valor representava, utilizei o site [Dcode](https://www.dcode.fr/en), especificamente a ferramenta [Cipher Identifier](https://www.dcode.fr/cipher-identifier). Ao inserir o valor encontrado nos metadados da imagem, o Dcode indicou que provavelmente se tratava de uma codificação `Base64`.

<img width="786" height="461" alt="image" src="https://github.com/user-attachments/assets/f5054262-dfee-445a-a107-ce0b8974cc4f" />

Em seguida, inseri o mesmo valor na ferramenta [Base64 Decoder](https://www.dcode.fr/base-64-encoding), também disponível no Dcode. Após realizar a decodificação, encontramos a informação secreta mencionada anteriormente no enunciado do desafio, que corresponde à FLAG:

`academy{the_m3tadata_1s_modified}`

<img width="786" height="434" alt="image" src="https://github.com/user-attachments/assets/67dc7453-10c0-49b6-84ec-c179b746057f" />

### Conclusão

Com a resolução desse desafio, foi possível compreender a importância dos metadados na análise forense de arquivos digitais. Essas informações podem armazenar dados que não são visíveis durante a utilização comum de um arquivo, podendo inclusive esconder informações importantes.

Utilizando o Exif.tools, conseguimos identificar um valor incomum nos metadados da imagem e, com o auxílio do Dcode, identificar sua codificação e realizar a decodificação em Base64, obtendo assim a FLAG necessária para concluir o desafio.
