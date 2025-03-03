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
        <url>https://raw.githubusercontent.com/theprogmatheus/maven-repository/master/</url>
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

## Como Usar Este Repositório no Seu Projeto Gradle

Para utilizar os artefatos deste repositório em seu projeto Gradle, siga os passos abaixo:

### 1. Adicione o Repositório ao `build.gradle`

Se estiver usando Gradle com `Groovy DSL`, adicione o seguinte bloco dentro da seção `repositories`:

```groovy
repositories {
    maven {
        url "https://raw.githubusercontent.com/theprogmatheus/maven-repository/master/"
    }
}
```

Se estiver usando Gradle com `Kotlin DSL`, adicione o seguinte bloco dentro da seção `repositories`:

```kotlin
repositories {
    maven {
        setUrl("https://raw.githubusercontent.com/theprogmatheus/maven-repository/master/")
    }
}
```

### 2. Adicione a Dependência do Artefato

Para adicionar uma dependência, utilize a seguinte sintaxe em seu `build.gradle`:

**Groovy DSL:**

```groovy
dependencies {
    implementation 'org.github.paperspigot:PaperSpigot:1.8.8-R0.1-SNAPSHOT-latest'
}
```

**Kotlin DSL:**

```kotlin
dependencies {
    implementation("org.github.paperspigot:PaperSpigot:1.8.8-R0.1-SNAPSHOT-latest")
}
```

## Artefatos Disponíveis

Atualmente, o repositório contém os seguintes artefatos:

| Artefato            | Versão                      | GroupID                                    |
| ------------------- | --------------------------  | -------------------------------------------|
| PaperSpigot         | 1.8.8-R0.1-SNAPSHOT-latest  | org.github.paperspigot                     |
| LegendChat          | 1.1.5                       | br.com.devpaulo.legendchat                 |
| PlaceholderAPI      | 2.9.2                       | me.clip.placeholderapi                     |
| Solary-Economy      | 1.5.3                       | com.redeskyller.bukkit.solaryeconomy       |
| itembuilder         | 1.0                         | com.github.theprogmatheus.minecraft.utils  |
| guibuilder          | 1.0                         | com.github.theprogmatheus.minecraft.utils  |
| Citizens            | 2.0.16-SNAPSHOT             | net.citizensnpcs                           |
| LuckPerms           | 5.4.156                     | net.luckperms.api                          |
| nChat               | 5.6.54                      | com.nickuc.chat                            |
| ProtocolLib         | 5.3.0                       | com.comphenix.protocol                     |
| SimpleClans         | 2.19.2-05e7abc              | net.sacredlabyrinth.phaed                  |
| Vault               | 1.7.3-b131                  | net.milkbowl.vault                         |
| WorldEdit           | 6.1.8-SNAPSHOT              | com.sk89q.worldedit.bukkit                 |
| WorldGuard          | 6.1-TRADUZIDA               | com.sk89q.worldguard.bukkit                |

Futuramente, outros artefatos podem ser adicionados conforme a necessidade.

---