<h1 align="center">🐉 Hydra ComicArchiveCreator BETA</h1>

<h3 align="center">Organize, converta e baixe seus mangás e quadrinhos em CBZ/CBR — tudo em um só lugar.</h3>

<p align="center">
  <img src="https://img.shields.io/badge/vers%C3%A3o-0.0.1-blue" alt="Versão 0.0.1">
  <img src="https://img.shields.io/badge/status-BETA-orange" alt="BETA">
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011%20(64--bit)-0078D6" alt="Windows">
  <img src="https://img.shields.io/badge/instala%C3%A7%C3%A3o-port%C3%A1til%20(portable)-brightgreen" alt="Portátil">
  <img src="https://img.shields.io/badge/tamanho-~80%20MB-lightgrey" alt="Tamanho">
  <img src="https://img.shields.io/badge/pre%C3%A7o-gratuito-success" alt="Gratuito">
</p>

---

## 📖 Sobre o projeto

O **Hydra ComicArchiveCreator BETA** é um aplicativo desktop para Windows feito para quem
coleciona, organiza e converte **capítulos de mangá/quadrinhos** em arquivos de leitura
digitais nos formatos **CBZ** e **CBR** (compatíveis com leitores como CDisplayEx,
YACReader, Komga, Kavita, Moon+ Reader, Tachiyomi e similares).

Com ele você consegue, sem usar linha de comando e sem instalar nada:

- 📦 Juntar capítulos soltos de imagens em **arquivos CBZ/CBR organizados**;
- 📚 Agrupar capítulos automaticamente em **volumes**;
- 🖼️ Converter **PDF** e **EPUB** em quadrinhos digitais;
- 🧩 **Mesclar** vários arquivos CBZ/CBR em um único arquivo;
- 🔎 **Buscar mangás** em fontes online e **baixar capítulos** escolhendo o idioma;
- ⚙️ Redimensionar, converter para JPG e otimizar as imagens.

> Este repositório distribui **apenas o executável (.exe)**.
> **O código-fonte não é público.** O aplicativo é gratuito.

---

## ⬇️ Download

1. Acesse a aba **[Releases](https://github.com/welligtonmal/HydraComicArchiveCreator/releases/latest)**.
2. Baixe o arquivo **`HydraComicArchiveCreatorBETA_v0.0.1.zip`**.
3. Extraia o ZIP em qualquer pasta.
4. Dê dois cliques em **`HydraComicArchiveCreatorBETA.exe`** e pronto! ✅

**Não é necessário instalar** Python, bibliotecas ou qualquer outro programa.
O aplicativo é **portátil**: pode ficar em um pendrive e funciona em qualquer PC.

---

## 💻 Requisitos

| Item | Detalhe |
|---|---|
| Sistema | **Windows 10 ou Windows 11 (64 bits)** |
| Espaço em disco | ~200 MB livres (para a primeira execução) |
| Internet | Necessária apenas para buscar/baixar mangás |
| WinRAR | **Opcional** — necessário somente para gerar arquivos `.cbr` |

---

## 🖼️ Prints do aplicativo

> 📌 **Para você:** crie a pasta `docs/screenshots/` no repositório e salve os prints com
> os nomes abaixo. As imagens aparecerão automaticamente aqui.

### Tela principal — Lotes de Capítulos
![Aba Lotes de Capítulos](docs/screenshots/01-lotes.png)

### Conversão de PDF
![Aba Conversão PDF](docs/screenshots/02-pdf.png)

### Conversão de EPUB
![Aba Conversão EPUB](docs/screenshots/03-epub.png)

### Mesclar Arquivos
![Aba Mesclar Arquivos](docs/screenshots/04-mesclar.png)

### Fontes Manga (busca e download)
![Aba Fontes Manga](docs/screenshots/05-fontes-manga.png)

### Sobre e Apoiar
![Aba Sobre e Apoiar](docs/screenshots/06-sobre-apoiar.png)

---

## ✨ O que cada função faz

### 📦 Aba "Lotes de Capítulos" — criar CBZ/CBR em lote

A ferramenta principal. Aponta uma pasta com vários capítulos (subpastas com imagens) e
gera os arquivos de leitura automaticamente.

| Campo | O que faz |
|---|---|
| **Pasta de entrada** | Pasta raiz onde estão os capítulos (cada subpasta = 1 capítulo). |
| **Pasta de saída** | Onde os arquivos CBZ/CBR serão salvos. |
| **Modo** | `chapter` = 1 arquivo por capítulo · `volume` = agrupa capítulos em volumes. |
| **Formato** | `cbz` (ZIP, não precisa de nada) ou `cbr` (RAR, requer WinRAR instalado). |
| **Capítulos por volume** | Quantos capítulos entram em cada volume (padrão: **10**). |
| **Manter pastas de capítulo no volume** | Mantém a separação por capítulo dentro do volume. |
| **Trabalhadores** | Quantas tarefas processam em paralelo (padrão: metade dos núcleos da CPU). |
| **Redimensionar (LxA)** | Redimensiona as imagens. Ex.: `1600x2400`. Deixe vazio para não alterar. |
| **Qualidade JPG** | Qualidade da conversão JPG (0–100, padrão: **92**). |
| **Converter para JPG** | Converte todas as imagens para `.jpg` antes de montar o arquivo. |
| **Sobrescrever** | Regera arquivos que já existem na pasta de saída. |
| **Usar cache** | Pula capítulos que não mudaram desde a última execução (padrão: **ligado**). |
| **Detalhado** | Exibe mensagens mais detalhadas do processamento. |
| **Executar Lote** | Inicia o processamento. |

**Destaques:** processamento em paralelo, baixo uso de memória (streaming), ignora
imagens corrompidas com aviso e cache inteligente para não repetir trabalho.

### 📄 Aba "Conversão PDF" — PDF → CBZ/CBR

Converte capítulos em PDF para o formato de quadrinho digital.

| Campo | O que faz |
|---|---|
| **Arquivo/Pasta PDF** | Selecione **um PDF** ou uma **pasta inteira** com vários PDFs. |
| **Pasta de saída** | Onde os arquivos convertidos serão salvos. |
| **Formato de saída** | `cbz` ou `cbr`. |
| **DPI** | Resolução das páginas renderizadas (padrão: **170**). Maior = melhor qualidade e arquivo maior. |
| **JPG quality** | Qualidade das imagens geradas (padrão: **90**). |
| **Executar PDF** | Inicia a conversão. |

### 📚 Aba "Conversão EPUB" — EPUB → CBZ

Converte eBooks `.epub` (incluindo mangás/quadrinhos em EPUB) para **CBZ**.

| Campo | O que faz |
|---|---|
| **Arquivo/Pasta EPUB** | Selecione **um EPUB** ou uma **pasta** com vários. |
| **Pasta de saída** | Onde os arquivos CBZ serão salvos. |
| **Executar EPUB** | Inicia a conversão. |

> A conversão segue a **ordem de leitura (spine)** do EPUB e extrai as páginas de imagem.

### 🧩 Aba "Mesclar Arquivos" — juntar CBZ/CBR

Junta vários arquivos em **um único arquivo** de quadrinho.

| Campo | O que faz |
|---|---|
| **Pasta com CBZ/CBR** | Pasta que contém os arquivos a mesclar. |
| **Arquivo de saída** | Caminho e nome do arquivo final. |
| **Formato de saída** | `cbz` ou `cbr`. |
| **Mesclar Arquivos** | Gera o arquivo unificado. |


### 🔎 Aba "Fontes Manga" — buscar e baixar capítulos

Pesquisa mangás em fontes online e baixa capítulos diretamente para o seu PC.

| Campo | O que faz |
|---|---|
| **Fonte** | `Todas`, `MangaDex`, `NoIndexScan`, `PinkRosa` ou `MangaBall`. |
| **Pesquisar** | Termo de busca (título do mangá) + botão **Buscar**. |
| **Mangás encontrados** | Lista de resultados. Clique em um resultado para ver os detalhes. |
| **Detalhes** | Título, fonte, URL e descrição do mangá selecionado. |
| **Carregar Capítulos** | Carrega a lista de capítulos do mangá escolhido. |
| **Idioma dos capítulos** | Seletor de idioma: *Todos*, **Português (Brasil)**, Português (Portugal), Inglês e Espanhol. |
| **Capítulos** | Lista de capítulos (mostra o idioma de cada um). |
| **Detalhes do capítulo** | Título, número, volume, idioma, URL e status do capítulo. |
| **Pasta de saída** | Onde os capítulos baixados serão salvos. |
| **Baixar Capítulo** | Baixa somente o capítulo selecionado. |
| **Baixar Todos** | Baixa todos os capítulos válidos da lista. |

**Sobre o seletor de idioma:** ao escolher um idioma, a busca já é filtrada na fonte
(MangaDex/MangaBall), evitando listas com capítulos de idiomas misturados. Trocar o idioma
recarrega a lista automaticamente.

### 💚 Aba "Sobre e Apoiar"

Informações do projeto, formas de apoiar o desenvolvimento (LivePix), comunidade e o bloco
de **publicidade** que mantém o app gratuito.

---

## 🗂️ Pastas criadas automaticamente

Na primeira execução, o app cria uma estrutura organizada em
`Documentos\HYDRA\`:

```
Documentos\
└── HYDRA\
    ├── Lotes\
    │   ├── Entrada\      ← coloque os capítulos aqui
    │   └── Saida\        ← arquivos CBZ/CBR gerados
    ├── PDF\
    │   ├── Entrada\
    │   └── Saida\
    ├── EPUB\
    │   ├── Entrada\
    │   └── Saida\
    ├── Mesclar\
    │   ├── Entrada\
    │   └── Saida\
    └── Manga\
        └── Downloads\    ← capítulos baixados das fontes
```

> Todos os caminhos são editáveis: você pode usar qualquer pasta do seu computador.

---

## 🚀 Como usar (passo a passo)

### Criar CBZ de capítulos soltos
1. Abra a aba **Lotes de Capítulos**.
2. Selecione a **Pasta de entrada** (com os capítulos) e a **Pasta de saída**.
3. Escolha o **Modo** (`chapter` ou `volume`) e o **Formato** (`cbz`/`cbr`).
4. (Opcional) Ajuste redimensionamento, qualidade e conversão para JPG.
5. Clique em **Executar Lote** e aguarde a barra de progresso.

### Converter PDF em CBZ
1. Aba **Conversão PDF** → selecione o arquivo ou a pasta de PDFs.
2. Defina a **Pasta de saída** e o **Formato de saída**.
3. Ajuste o **DPI** conforme a qualidade desejada e clique em **Executar PDF**.

### Baixar um mangá
1. Aba **Fontes Manga** → escolha a **Fonte** e digite o nome do mangá.
2. Clique em **Buscar** e selecione o resultado correto.
3. Escolha o **Idioma dos capítulos** e clique em **Carregar Capítulos**.
4. Selecione a **Pasta de saída** e clique em **Baixar Capítulo** (ou **Baixar Todos**).

---

## 💡 Dicas e limitações

- **CBR requer WinRAR** instalado no PC. Se não tiver, use **CBZ** (funciona em qualquer leitor).
- A **primeira abertura** pode demorar alguns segundos a mais (o app se prepara em segundo plano);
  as próximas abrem mais rápido.
- Ao abrir, o Windows pode exibir o aviso **"Windows protegeu seu computador"** (SmartScreen).
  Isso é normal em programas gratuitos sem certificado digital: clique em
  **"Mais informações" → "Executar assim mesmo"**.
- Capítulos marcados como **[Indisponível]** ou **[Externo]** não podem ser baixados pelo app.
- Fontes online podem ficar em manutenção temporariamente — tente novamente mais tarde.


---

## ❓ Perguntas frequentes (FAQ)

**O app precisa de Python ou de alguma instalação?**
Não. O executável é totalmente independente: é só baixar e executar.

**É seguro? Meu antivírus reclamou.**
Alguns antivírus alertam por precaução em programas novos/portáteis sem assinatura digital.
O app apenas organiza/converte seus arquivos e baixa de fontes públicas de mangá. Você pode
adicionar a pasta do app como exceção no antivírus, se desejar.

**Funciona em Windows 32 bits, Linux ou Mac?**
Atualmente **não**. Esta versão é para **Windows 10/11 de 64 bits**.

**Onde os arquivos são salvos?**
Na pasta que você escolher. Por padrão, tudo fica organizado em `Documentos\HYDRA\`.

**Posso desativar o anúncio?**
O anúncio aparece no máximo **1 vez por dia**, ao iniciar o app, e é o que mantém o projeto
gratuito. Ele nunca abre janelas sozinho além dessa, e não coleta seus dados.

**O aplicativo baixa os mangás sozinho?**
Ele consulta as fontes no momento em que você pesquisa/escolhe — nada é baixado sem a sua ação.

**Serve para qualquer formato de imagem?**
Sim: JPG, PNG, WebP, BMP, GIF, TIFF — o app converte/valida automaticamente.

---

## 💚 Apoie o projeto

O Hydra ComicArchiveCreator é **gratuito** e mantido pela comunidade. Se ele te ajuda,
considere apoiar o desenvolvimento:

- 💙 **LivePix:** [livepix.gg/hydraani](https://livepix.gg/hydraani)

Sua ajuda mantém os servidores, as fontes atualizadas e novas funcionalidades chegando. 🐉

---

## 🌐 Comunidade

- 📝 **Blogger:** [hydraani.blogspot.com](https://hydraani.blogspot.com/)
- 💬 **Telegram:** [t.me/+Ro3nukr5CjU0NTRh](https://t.me/+Ro3nukr5CjU0NTRh)
- 🤖 **Grupo Android Hydra Ani:** [t.me/+p7-RyWDRRVhlMTdh](https://t.me/+p7-RyWDRRVhlMTdh)

---

## 📋 Changelog

### v0.0.1 (BETA) — primeira versão pública
- 📦 Criação de CBZ/CBR por capítulo ou por volume, com processamento paralelo.
- 🖼️ Redimensionamento e conversão para JPG com qualidade ajustável.
- 🔁 Cache inteligente para pular arquivos inalterados.
- 📄 Conversão de **PDF** e **EPUB** para CBZ/CBR.
- 🧩 Mesclagem de vários CBZ/CBR em um arquivo.
- 🔎 Busca em **MangaDex, NoIndexScan, PinkRosa e MangaBall**.
- 🌍 **Seletor de idioma** dos capítulos (Todos, pt-BR, pt-PT, Inglês, Espanhol).
- ⬇️ Download de capítulos individuais ou de todos de uma vez.
- 🆓 Instalador portátil (~80 MB) — não requer instalação.
- 🎨 Ícone e identidade visual próprios.

---

## ⚖️ Licença e aviso legal

- **Licença:** *Freeware* — o aplicativo é gratuito para uso pessoal.
  **O código-fonte não é distribuído publicamente**; este repositório publica apenas os
  executáveis oficiais. É proibida a revenda ou redistribuição modificada sem autorização.
- **Aviso legal:** o aplicativo **não hospeda nenhum conteúdo**. Ele apenas organiza,
  converte e baixa arquivos de fontes públicas de terceiros. Todo o conteúdo baixado é de
  responsabilidade do usuário e deve respeitar as leis de direitos autorais do seu país.
  Apoie os autores e editoras oficiais sempre que possível.
- **Privacidade:** o aplicativo não coleta dados pessoais. A publicidade exibida
  (Adsterra) é um anúncio de terceiros aberto no navegador, no máximo 1 vez por dia.

---

<p align="center">
  Feito com 💙 e ☕ por <b>Hydra Animes</b><br>
  <i>Hydra ComicArchiveCreator BETA v0.0.1</i>
</p>

<p align="center">
  <a href="https://livepix.gg/hydraani"><img src="https://img.shields.io/badge/Apoiar-LivePix-00b894" alt="Apoiar"></a>
  <a href="https://hydraani.blogspot.com/"><img src="https://img.shields.io/badge/Blogger-hydraani-orange" alt="Blogger"></a>
  <a href="https://t.me/+Ro3nukr5CjU0NTRh"><img src="https://img.shields.io/badge/Telegram-Comunidade-2CA5E0" alt="Telegram"></a>
</p>

