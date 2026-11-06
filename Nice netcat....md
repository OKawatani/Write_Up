# Nice netcat...

**Categoria:** Misc

**Autor:** syreal

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/156?page=1&search=nice&workspace=true), possui a seguinte descrição:

> There is a nice program that you can talk to by using this command in a shell:
>
> nc xebec.cylabacademy.net 42433
>
> but it doesn't speak English...

### Resolução

Ao iniciar a instância, que é gerada aleatoriamente toda vez que o desafio é iniciado, recebemos a seguinte linha de comando: `nc xebec.cylabacademy.net 42433`. Ao executar esse comando no terminal fornecido pela própria plataforma CyLab, recebemos uma sequência de números aparentemente aleatórios.

<img width="443" height="595" alt="image" src="https://github.com/user-attachments/assets/92c1266d-44e7-439d-856c-0071ff69e7e7" />

Uma sequência de números aparentemente aleatórios pode representar algum tipo de codificação. Para descobrir do que se tratava, utilizei o site [Dcode](https://www.dcode.fr/en), especificamente a ferramenta [Cipher Identifier](https://www.dcode.fr/cipher-identifier). Ao inserir a sequência numérica recebida anteriormente, obtivemos um resultado indicando que o código provavelmente se tratava de uma codificação ASCII.

<img width="792" height="469" alt="image" src="https://github.com/user-attachments/assets/26266b1a-bbb2-4a67-b343-adab597961cd" />

Em seguida, inseri a mesma sequência na ferramenta [ASCII Converter](https://www.dcode.fr/ascii-code), também disponível no Dcode. Após realizar a conversão, conseguimos obter a FLAG do desafio:

`academy{g00d_k1tty!_n1c3_k1tty!_57380}`

<img width="776" height="453" alt="image" src="https://github.com/user-attachments/assets/58f68a15-8ae3-4af9-bc05-239b64a94ed7" />

### Conclusão

Com a resolução desse desafio, foi possível compreender como uma sequência de números pode representar caracteres por meio da codificação ASCII. Além disso, o desafio demonstrou a importância de identificar o tipo de codificação utilizado antes de tentar interpretar uma informação.

Utilizando as ferramentas disponibilizadas pelo site Dcode, conseguimos identificar e converter a sequência numérica, obtendo a FLAG necessária para concluir o desafio.
