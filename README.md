#  ITassist — Sistema de Gestão de Suporte e Infraestrutura de TI

<p align="center">
  <b>Plataforma centralizada para otimização de chamados técnicos, controlo de ativos e gestão de atendimento de TI.</b>
</p>

---

##  Sobre o Projeto
O **ITassist** é uma aplicação desenvolvida no âmbito acadêmico (UNISO) com o objetivo de solucionar os gargalos na gestão de suporte técnico empresarial. O sistema permite o registo estruturado de chamados, triagem por categorias, alocação de técnicos especializados e histórico cronológico de interações.

---

##  Equipa de Desenvolvimento
* **Gabriel Augusto** — Engenharia e Gestão da Base de Dados
* **Pedro** — Desenvolvimento / Back-end
* **João** — Desenvolvimento / Front-end / Integrações
* **Rafael** — Arquitetura e Testes

---

## Arquitetura da Base de Dados (PostgreSQL)
A base de dados relacional (`itassist_db`) foi modelada e implementada utilizando **PostgreSQL** e gerida via **pgAdmin 4**[cite: 7, 8]. 

A estrutura é composta por **6 tabelas principais**:
1. **`setores`**: Mapeamento dos departamentos da organização[cite: 7].
2. **`usuarios`**: Cadastro unificado de credenciais e colaboradores[cite: 7].
3. **`tecnicos`**: Extensão dos utilizadores com especialidades e disponibilidade[cite: 7].
4. **`categorias`**: Classificação temática dos incidentes e requisições[cite: 7].
5. **`chamados`**: Tabela central de gestão do ciclo de vida dos tickets (status, prioridade, impacto e prazos)[cite: 7].
6. **`interacoes_chamado`**: Registo cronológico de conversas e atualizações de cada ticket[cite: 7].

###  Diagrama Entidade-Relacionamento (DER)
> *(O diagrama completo da base de dados encontra-se documentado na pasta de documentação do projeto e visualizado via pgAdmin).*

---

##  Como Restaurar a Base de Dados (Para a Equipa)

Se precisares de configurar a base de dados no teu ambiente local através do backup fornecido (`.sql`), segue os passos abaixo no **pgAdmin 4**:

1. Abre o **pgAdmin 4** no teu computador.
2. Cria uma nova base de dados vazia com o nome `itassist_db`:
   * Clica com o botão direito em **Databases** > **Create** > **Database...**
   * Nome: `itassist_db` e clica em *Save*.
3. Restaura o ficheiro de backup:
   * Clica com o botão direito em cima da nova base de dados `itassist_db`.
   * Seleciona **Restore...**
   * Em *Filename*, seleciona o ficheiro `.sql` de backup incluído no repositório.
   * Clica no botão **Restore**.

---

## 🚀 Tecnologias Utilizadas
* **Banco de Dados:** PostgreSQL[cite: 7]
* **Ferramenta de Gestão:** pgAdmin 4[cite: 7]
* **Controlo de Versão:** Git & GitHub
