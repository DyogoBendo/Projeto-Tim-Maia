# Projeto Tim-Maia

Você já quis aprender __Inglês__? Ou já quis aprender sobre os __países__ ao redor do mundo? Agora, imagina se você pudesse aprender os dois em conjunto. Sim, você pode! E você está no lugar certo!

## Objetivo

O objetivo do nosso projeto é criar um __website__ para o ensino de Inglês em conjunto com o ensino de aspectos históricos, culturais, demográficos, econômicos, geográficos e políticos dos páises ao redor do mundo.

## Estrutura das pastas

### Sitemap

Primeiramente, para entender a estruturação das pastas, é preciso entender a estrutura do website:

![Paisagem][sitemap]

* [__Link__ para abrir o sitemap diretamente no whimsical][sitemaplink]

Bom, visto isso, podemos começar a entender a estruturação

### Estrutura

O projeto tem 6 pastas principais: 3 páginas são relacionadas a cógigos e scripts, e as outras 3 páginas para a estruturação das rotas do website. Os repositórios para o armazenamento de scripts e outros são reconhecido pelo `'_' (underline)` antes dos nomes

```text
Projeto Tim-Maia
 |- _assets
 |- _medias
 |- _static
 |- AboutUs
 |- Tutorial
 |- WorldMap
 |- index.html
 |- README.md
```

#### Diretórios de scripts e medias

* ___assets__: Esse diretório irá conter as imagens usadas para a documentação e os `README.md` do projeto;

* ___medias__: Diretório responsável por armazar os arquivos de mídia que serão utilizados na pagina home `(index.html)`. Esse diretório é subdivido em outros 3 subrepositórios:

    ```text
    _medias
     |- audios
     |- images
     |- videos
    ```

    * __audios__: resposável por armazernar os aúdios;
    * __images__: responsável por armazernar as images. Esse diretório é divido em um subdiretório `icons`. Este, por sua vez, armazena os icones que serão utilizados na `home`;
    * __videos__: responsável por armazernar os videos. Esse _dir_, também é subdivido igual o _dir images_. No entanto o _subdir_ é o `captions`. Este por sua vez, armazena as legendas dos vídeos.

* __static__: Este diretório é um dos mais importantes do projeto. Nele temos um _subdir_ chamado `global`. Nesse _subdir_, serão armazenados os scripts e folhas de estilo globais, que serão usados em todas as páginas. A funcionalidade desses arquivos serão parecidos com o _bootstrap_. Uma particularidade do _subdir_ `scripts` é seu outro _subdir_ `utils`
    
    * __utils__: Nesse arquivo é onde será declarados os modúlos mais gerais, como p. ex.: verificar se o dark mode está ativo na página. Ou também, diminuir a luminosidade das cores do site;

#### Diretórios referentes a rotas

* __AboutUs__: Essa rota/diretório é responsável por armazenar a página `About Us`, mostrado no sitemap do projeto. A estrutura dele segue a estrutura que será utilizada no diretório de `Tutorial`

    ```text
    AboutUs
     |- _medias
     |- index.html
     |- README.md
     |- script.js
     |- styles.css
    ```

    * __OBS__: O diretório de `_medias` segue a mesma estrutura do _subdir_ `_medias` que é _subdir_ direto do diretório principal do projeto.

* __Tutorial__: Rota responsável por apresentar um tutorial sobre as funcionalidades e como usar o website. O tutorial também tem seus diretórios que não são referentes as rotas do website. Esses diretórios seguem o mesmo modelo dos anteriores. Além disso, o `Tutorial` é divido em duas partes, cada uma referente a um _subdir_

    ```text
    Tutorial
     |- _medias
     |- _static
     |- Geral
     |   |- tutorial.html
     |- Specific
     |   |- Country
     |   |   |- tutorial.html
     |   |- HowToStudy
     |   |   |- tutorial.html
     |   |- WorldMap
     |   |   |- tutorial.html
     |- index.html
     |- script.js
     |- styles.css
    ```

    * __Geral__: A rota `Geral` irá apresentar um tutorial do inicio até o fim
    * __Specific__: Já a rota `Specific` irá dar a possibilidade do usuário escolher que parte do website deseja obter ajuda. O tutorial especifico está divido em 3 partes: _Country_, _How to Study_ e _WorldMap_;

        * __OBS__: A estilização de todos os tutoriais será armazenado no diretório `_static` do diretório `Tutorial`. O motivo disso, é porque haverá uma padronização, pois o estilo de cada página ja estará pronta e no tutorial só será preciso adicionar alguns _popups_

* __WorldMap__: A principal rota do website é a rota de `WorldMap`. Nela teremos uma página `index.html`, que irá redirecionar o usuário ao páis que este selecionar no _world map_.

    * O diretório `WorldMap` é divido pelos continentes, e por sua vez, os continetes são dividos pelos países que irão compor o website

    * Essa é a seguinte estruturação do diretório `WorldMap`:

    ```text
    WorldMap
     |- _static
     |- Africa
     |-  |- Egypt
     |-  |- Kenya
     |-  |- Nigeria
     |-  |- SouthAfrica
     |- America
     |-  |- Brazil
     |-  |- Canada
     |-  |- Caribbean
     |-  |- UnitedStates
     |- Asia
     |-  |- CHT (China - Hong Kong - Taiwan)
     |-  |- IPB (India - Paquistão - Bangladesh)
     |-  |- Japan
     |-  |- Koreas
     |- Europe
     |-  |- France
     |-  |- Germany
     |-  |- Switzerland
     |-  |- UKIE (United Kingdom - Ireland)
     |- Oceania
     |-  |- Australia
     |-  |- NewZealand
     |- index.html
     |- script.js
     |- styles.css
    ```

    * Os diretórios dos países seguem uma estrutura padrão que segue em todos eles. Para exemplificar, vamos utilizar o `Egypt`

        ```text
        Africa
         |- Egypt
         |   |- Culture
         |   |   |- _medias
         |   |   |- culture.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- Demography
         |   |   |- _medias
         |   |   |- demography.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- Economy
         |   |   |- _medias
         |   |   |- economy.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- Geography
         |   |   |- _medias
         |   |   |- geography.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- History
         |   |   |- _medias
         |   |   |- history.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- Policy
         |   |   |- _medias
         |   |   |- policy.html
         |   |   |- script.js
         |   |   |- styles.css
         |   |- index.html
        ```

    * Cada tópico de um país têm um arquivo `.html`, `.css` e `.js`, respectivo as particulariedades daquela página do tópico. Além disso, como padrão, cada tópico tem um _subdir_ `_medias`

## Colaboradores

Somos estudantes do 2 ano do curso Técnico em Informática integrado ao Ensino Médio do Instituto Federal do Paraná (IFPR), Campus Foz do Iguaçu.

* [Dyogo Bendo][dyogogithub]
* [Vinicius Jimenez][viniciusgithub]
* [Nikoly Cover][nikolygithub]
* [Daniel Chielle][danielgithub]

[dyogogithub]: https://github.com/DyogoBendo "DyogoBendo GitHub"
[viniciusgithub]: https://github.com/DyogoBendo "vinniciusJ GitHub"
[nikolygithub]:  https://github.com/KolyCover "KolyCover GitHub"
[danielgithub]:  https://github.com/LeinadRPFI "LeinadRPFI GitHub"

[sitemaplink]: https://whimsical.com/4KkJ2RteCM67tV6mHiDCoU "Abrir diretamente no whimsical"
[sitemap]:_assets/sitemap.png