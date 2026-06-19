# Modelo de TCC - CESAR School 🎓

Este repositório contém o modelo oficial customizado em LaTeX para a elaboração de Trabalhos de Conclusão de Curso (TCC), Dissertações ou Projetos de Pesquisa da **CESAR School**. 

O projeto foi estruturado de forma modular e limpa, separando as regras de formatação visual do conteúdo textual do seu trabalho.

---

## 📁 Estrutura do Repositório

Com base na organização real do projeto, os arquivos estão distribuídos da seguinte forma:

```text
├── main.tex                 # Arquivo principal que gerencia e compila o projeto
├── references.bib           # Banco de dados das suas citações (BibTeX)
├── config/                  # Configurações estéticas globais do modelo
│   ├── fonts.tex            # Definição da fonte principal (Arial 12)
│   ├── page.tex             # Configuração de margens, entrelinhas, cabeçalhos e rodapés
│   ├── sections.tex         # Estilização e recuos de seções, subseções e títulos
│   └── lists.tex            # Customização do Sumário, Lista de Figuras/Tabelas e pontinhos
├── extra/                   # Arquivos de suporte e ferramentas extras
│   └── notas.tex            # Arquivo centralizador para notas de rodapé limpas
├── images/                  # Pasta destinada ao armazenamento de figuras do trabalho
│   └── logo.png             # Logo da instituição
└── sections/                # Conteúdo textual numerado do seu TCC
    ├── 00-capa.tex          # Capa do trabalho
    ├── 01-contra-capa.tex   # Folha de rosto
    ├── 02-resumo.tex        # Resumo na língua nativa (Português)
    ├── 03-abstract.tex      # Resumo na língua estrangeira (Inglês)
    ├── 04-lista-imagens.tex # Lista automática de ilustrações (sem número de página físico)
    ├── 05-lista-tabelas.tex # Lista automática de tabelas (sem número de página físico)
    ├── 06-sumario.tex       # Sumário automático (com pontinhos nas seções em negrito)
    ├── 07-introducao.tex    # Introdução (onde a numeração começa a aparecer no topo à direita)
    ├── 08-fundamentacao-teorica.tex
    ├── 09-desenvolvimento.tex
    ├── 10-conclusao.tex
    ├── 11-referencias.tex   # Renderização do BibTeX mapeada no Sumário
    ├── 12-apendices.tex     # Elementos pós-textuais (ocultados automaticamente do Sumário)
    └── 13-anexos.tex        # Elementos pós-textuais (ocultados automaticamente do Sumário)

```

---

## 🚀 Como Executar e Usar no Overleaf

Como este modelo usa recursos tipográficos modernos (como o pacote `fontspec` para carregar a fonte Arial nativa do sistema), ele precisa de motores de renderização específicos.

1. Baixe o código deste repositório em formato ZIP (**Code > Download ZIP**).
2. Vá para o seu painel do [Overleaf](https://www.overleaf.com/) e crie um novo projeto importando esse ZIP (**New Project > Upload Project**).
3. **⚙️ Ajuste Obrigatório do Compilador:**
* No canto superior esquerdo da tela do Overleaf, clique no botão **Menu**.
* Procure a opção **Compiler** (Compilador).
* Mude de *pdfLaTeX* para **XeLaTeX** (ou *LuaLaTeX*).


4. Clique em **Recompile** (Recompilar) e o documento gerará o PDF perfeitamente.

---

## 🛠️ Soluções de Layout Implementadas

Este template já resolve nativamente as principais dores de cabeça de formatação exigidas pelas bancas de avaliação:

* **Numeração Inteligente:** A paginação é calculada invisivelmente desde os elementos iniciais (Capa, Resumos, Listas). O número impresso no papel só começa a aparecer de fato no **topo à direita** a partir da página da `Introdução`.
* **Sumário Corrigido:** Linhas guia pontilhadas interligam perfeitamente os títulos em negrito até seus respectivos números de página.
* **Filtro de Apêndices e Anexos:** Eles geram páginas normais ao final do documento (`12-apendices` e `13-anexos`), mas somem automaticamente do Sumário para não poluir o escopo principal do trabalho.
* **Notas de Rodapé Despoluídas:** Você pode declarar os textos de termos técnicos longos dentro do diretório de suporte em `extra/notas.tex` e apenas invocar os comandos nos capítulos, mantendo a leitura do seu código LaTeX impecável.

---

## ✍️ Guia de Escrita

* **Para escrever o conteúdo:** Não altere a estrutura da `main.tex`. Escreva diretamente nos arquivos correspondentes dentro da pasta `sections/`.
* **Para referências bibliográficas:** Alimente o seu arquivo `references.bib` com as entradas BibTeX coletadas de plataformas como o Google Acadêmico e utilize o comando `\cite{chave}` no meio do texto.
* **Para criar notas explicativas:** Abra o arquivo `extra/notas.tex`, declare uma variável usando `\newcommand{\minhanota}{Sua explicação aqui}` e no texto aplique `\footnote{\minhanota}`.

```

```
