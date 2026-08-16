# Minicurso - Uso e Customização de Pipelines nf-core

## Lesson overview 📚

|  |  |
| :--- | :--- |
| **Licença** | [Creative Commons Attribution Share Alike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/deed.en) |
| **Público-alvo** | Alunos de graduação e pós-graduação, pesquisadores e profissionais de bioinformática. |
| **Nível** | **Iniciante/Intermediário** |
| **Tempo estimado** | 300 minutos (5 horas) |
| **Material do curso** | [](https://dalmolingroup.github.io/nextflow_training/) |

---

## 📖 Descrição do Curso

Este repositório contém o material do minicurso **"Uso e Customização de Pipelines nf-core"**. O objetivo é capacitar quem trabalha com bioinformática a **executar, configurar e customizar pipelines nf-core existentes** — a demanda mais comum no dia-a-dia de quem processa dados ômicos.

O curso é baseado no material oficial da [Nextflow Training](https://training.nextflow.io/), adaptado e condensado para 5 horas com foco em customização (não em desenvolvimento).

O curso cobre as seguintes etapas essenciais:

1.  **Fundamentos do Nextflow:** Estrutura de um pipeline (processos, canais, workflow, módulos), execução, inspeção de logs (`.command.*`), `-resume` e ciclo de vida de execuções.
2.  **Configuração:** `nextflow.config`, diretivas de processo, profiles, `-params-file`, ordem de precedência e inspeção da configuração resolvida.
3.  **nf-core na prática:** O que é nf-core, `nextflow pull`, estrutura de um pipeline nf-core, perfil de teste e interpretação da execução.
4.  **Customização:** Parâmetros vs. configuração, `--help` via schema, `-params-file`, arquivos de configuração personalizados com `-c` e o padrão-chave `ext.args` para passar argumentos extras às ferramentas.
5.  **Validação de entradas:** Schemas de parâmetros e de samplesheet (nf-schema), debug de erros comuns antes de qualquer processo executar.
6.  **Módulos nf-core:** Catálogo de módulos reutilizáveis, `nf-core modules install/info/update` e customização por `ext.args`.

---

## ➡ Resultados de Aprendizagem

Ao final do curso, os alunos serão capazes de:

1.  **Entender** a estrutura básica de um pipeline Nextflow (processos, canais, workflow, módulos, contêineres).
2.  **Executar** pipelines nf-core prontos usando perfis de teste e produção.
3.  **Configurar** a execução via `params`, `-params-file` e arquivos de configuração personalizados.
4.  **Personalizar** recursos computacionais e argumentos de ferramentas usando o padrão `ext.args`.
5.  **Instalar** e **usar** módulos do repositório nf-core em pipelines existentes.
6.  **Diagnosticar** erros comuns a partir das mensagens de validação de schema e samplesheet.

---

## ⚙  Requisitos de Software

Participantes devem ter um laptop com as ferramentas abaixo instaladas — ou usar o ambiente pré-configurado no [GitHub Codespaces](https://codespaces.new/nextflow-io/training?quickstart=1).

### 📦 Dependências principais

| Categoria | Ferramenta | Versão mínima |
| :--- | :--- | :--- |
| **Engine** | [Nextflow](https://www.nextflow.io/) | 25.10.2+ |
| **Contêineres** | [Docker](https://www.docker.com/) (ou Singularity/Apptainer) | — |
| **nf-core** | [`nf-core tools`](https://nf-co.re/tools) | 4.0.2+ |
| **Java** | JDK (necessário para o Nextflow) | 11+ |

### Instalação rápida (Linux/macOS)

```bash
# 1. Java (pré-requisito do Nextflow) — use SDKMAN ou o gerenciador do seu sistema
curl -s https://get.sdkman.io | bash
sdk install java 17.0.10-tem

# 2. Nextflow
curl -s https://get.nextflow.io | bash
sudo mv nextflow /usr/local/bin/
nextflow -version

# 3. Docker — siga o guia oficial para sua distribuição
# https://docs.docker.com/engine/install/

# 4. nf-core tools
pip install nf-core
nf-core --version
```

### Alternativa sem instalação

Use o [GitHub Codespace](https://codespaces.new/nextflow-io/training?quickstart=1) mantido pela Seqera — já vem com tudo pronto, incluindo VS Code no navegador.


---

## 🙏 Agradecimentos

* **[Seqera Labs](https://seqera.io/)** — desenvolvedores e mantenedores do Nextflow, cujo trabalho open source é a base de todo este material.
* **[Comunidade nf-core](https://nf-co.re/)** — pela curadoria colaborativa dos pipelines, módulos e configurações institucionais que tornam a bioinformática reprodutível acessível a todos.
* **[Nextflow Training](https://training.nextflow.io/)** — este minicurso é uma adaptação condensada do material oficial mantido pela Seqera e pela comunidade nf-core, com foco em uso e customização.
* **Bioinformatics Multidisciplinary Environment** (BioME - IMD/UFRN)
* **Postgraduate Program in Bioinformatics** (PPg-Bioinfo - UFRN)
