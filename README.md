# Maven Repository

Este repositório no GitHub funciona como um repositório Maven para hospedar artefatos que serão utilizados em alguns dos meus projetos. Ele permite que qualquer desenvolvedor que precise desses artefatos os utilize diretamente em seus projetos Maven, sem precisar hospedar os arquivos localmente.

## Como Usar Este Repositório no Seu Projeto Maven

Para utilizar os artefatos deste repositório em seu projeto Maven, é necessário adicionar este repositório ao arquivo `pom.xml`. Siga os passos abaixo:

### 1. Adicione o Repositório ao `pom.xml`

Adicione a seguinte configuração dentro da tag `<repositories>` no seu `pom.xml`:

```xml
<repositories>
    <repository>
        <id>github-theprogmatheus-maven-repository</id>
        <url>https://github.com/theprogmatheus/maven-repository/raw/refs/heads/master/</url>
    </repository>
</repositories>
```

### 2. Adicione a Dependência do Artefato

Após adicionar o repositório, inclua a dependência desejada na seção `<dependencies>` do seu `pom.xml`. Por exemplo, para utilizar o `PaperSpigot 1.8.8`, adicione:

```xml
<dependency>
    <groupId>org.github.paperspigot</groupId>
    <artifactId>PaperSpigot</artifactId>
    <version>1.8.8-R0.1-SNAPSHOT-latest</version>
    <scope>provided</scope>
</dependency>
```

> **Nota:** Como os arquivos estão hospedados no GitHub de forma manual, pode ser necessário limpar o cache do Maven para garantir que ele baixe a versão mais recente. Para isso, execute:
>
> ```sh
> mvn clean install
> ```

## Artefatos Disponíveis

Atualmente, o repositório contém os seguintes artefatos:

| Artefato            | Versão                      | GroupID                           |
| ------------------- | --------------------------  | --------------------------------- |
| PaperSpigot         | 1.8.8-R0.1-SNAPSHOT-latest  | org.github.paperspigot            |
| LegendChat          | 1.1.5                       | br.com.devpaulo.legendchat        |
| PlaceholderAPI      | 2.9.2                       | me.clip.placeholderapi            |

Futuramente, outros artefatos podem ser adicionados conforme a necessidade.

---