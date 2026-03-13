# modelagem-bd-publicacoes-cientificas
# Projeto de Modelagem de Dados: Sistema de Gestão de Publicações Científicas

## 📌 Sobre o Projeto
Este repositório contém o projeto de modelagem de banco de dados relacional desenvolvido para um Sistema de Gestão de Publicações Científicas. O objetivo da arquitetura é organizar e rastrear o relacionamento complexo entre periódicos, editoras, artigos publicados e pesquisadores (autores).

O escopo do projeto abrange as fases fundamentais da engenharia de dados, garantindo a integridade referencial e a normalização das regras de negócio antes da implementação física.

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Engenharia de Dados:** Modelagem Conceitual e Modelagem Lógica.
* **Ferramenta de Modelagem:** brModelo.
* **Controle de Versão:** Git / GitHub.

## 📊 Arquitetura de Dados

### 1. Modelo Conceitual (Diagrama Entidade-Relacionamento - DER)
Nesta etapa, foram mapeadas as entidades principais e suas cardinalidades para atender aos requisitos do sistema:
* **Periódicos e Editoras:** Um periódico pertence a uma editora, e uma editora pode publicar vários periódicos.
* **Artigos:** Relacionados estritamente aos periódicos em que foram publicados (com atributos como DOI).
* **Pesquisadores:** Mapeamento da autoria de artigos (relação N:N, onde um artigo pode ter vários autores, e um autor pode escrever vários artigos, utilizando identificadores como ORCID).



### 2. Modelo Lógico
Tradução do modelo conceitual para a estrutura relacional, definindo rigorosamente:
* **Tipagem de dados:** Uso de `INT` para identificadores numéricos (como `id_artigo`, `id_editora` e `orcid`) e `VARCHAR` para campos de texto e códigos específicos (como `issn`, `DOI`, nomes e país).
* **Chaves Primárias (PK):** Para identificação única de registros garantindo a consistência da base.
* **Resolução de Cardinalidade:** Criação da tabela associativa `Autor -de` para resolver a relação N:N entre `Artigo` e `Pesquisador`, com a devida aplicação de Chaves Estrangeiras (FK) duplas para manter a integridade referencial.

* <img width="876" height="499" alt="Captura de tela 2026-03-05 172220" src="https://github.com/user-attachments/assets/c1cc265e-d07f-4ad7-ae73-7050ba8a7416" />

## 📂 Arquivos do Projeto
  : Exportação visual do DER.

<img width="876" height="499" alt="DIAGRAMA LOGICO ARTI" src="https://github.com/user-attachments/assets/86ee585f-0734-4d87-8a63-b7d27e2cc6e3" />   
: Exportação visual do modelo relacional lógico.

## 👨‍💻 Autor

Projeto desenvolvido por **Iago Nicolas Santos Schwarz**

