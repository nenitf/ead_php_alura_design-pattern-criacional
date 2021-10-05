# ead_php_alura_design-pattern-criacional

> Projeto referente a [este](https://cursos.alura.com.br/course/php-design-pattern-criacional) curso.

1. Crie o ambiente
```sh
docker-compose up -d
```
> Caso queira, ao final da configuração, pare o Docker com ``docker-compose down``

2. Crie o autoloader
```sh
docker-compose exec app composer du
```

## Execução

- Caso recém tenha feito a **configuração inicial** e o ambiente continue rodando, tudo certo. Pode acessar ``localhost:8989/arquivo-script.php``
- Do contrário, suba o ambiente novamente:
```sh
docker-compose up
```
> Pare com <kbd>Ctrl</kbd><kbd>C</kbd>

> Caso modifique Dockerfile, rebuilde com ``docker-compose up --build``

> Para acessar o container use ``docker-compose exec app bash`` ou execute os scripts diretamente pelo Docker ``docker-compose exec app php public/arquivo-script.php``

## Anotações

- [Comparação de Factories](https://refactoring.guru/pt-br/design-patterns/factory-comparison)

---

- **Flyweight Factory** cria ou reutiliza objetos, o algoritmo consiste em:
    1. criar um array com todos já criados e alguma chave única que os defina
    2. quando precisar criar um objeto testar se a chave existe
    3. caso exista, deve retornar o objeto do array pela chave, do contrário deve criar ele conforme o passo 1
- **Factory Method** semelhante ao template method, executa um algoritmo que depende de um método abstrato que deve ser implementado pela classe filha. Útil para reutilizar código ao invés de múltiplas factories com uma linha de diferença
- **Abstract Factory** interface comum de vendas com intenção comum
