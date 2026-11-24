#  ITassist — Sistema de Gestão de Suporte e Infraestrutura de TI

<p align="center">
  <b>Plataforma centralizada para otimização de chamados técnicos, controle de ativos e gestão de atendimento de TI.</b>
</p>

---

##  Sobre o Projeto
O **ITassist** é uma aplicação desenvolvida no âmbito acadêmico (UNISO) com o objetivo de solucionar os gargalos na gestão de suporte técnico empresarial. O sistema permite o registro estruturado de chamados, triagem por categorias, alocação de técnicos especializados e histórico cronológico de interações.

---

##  Equipe de Desenvolvimento
* **Gabriel Augusto** — Engenharia e Gestão do Banco de Dados
* **Pedro** — Desenvolvimento / Back-end
* **João** — Desenvolvimento / Front-end / Integrações
* **Rafael** — Arquitetura e Testes

---

## Arquitetura do Banco de Dados (PostgreSQL)
O banco de dados relacional (`itassist_db`) foi modelado e implementado utilizando **PostgreSQL** e gerenciado via **pgAdmin 4**. 

A estrutura é composta por **6 tabelas principais**:
1. **`setores`**: Mapeamento dos departamentos da organização.
2. **`usuarios`**: Cadastro unificado de credenciais e colaboradores.
3. **`tecnicos`**: Extensão dos usuários com especialidades e disponibilidade.
4. **`categorias`**: Classificação temática dos incidentes e requisições.
5. **`chamados`**: Tabela central de gestão do ciclo de vida dos tickets (status, prioridade, impacto e prazos).
6. **`interacoes_chamado`**: Registro cronológico de conversas e atualizações de cada ticket.

###  Diagrama Entidade-Relacionamento (DER)
> *(O diagrama completo do banco de dados encontra-se documentado na pasta de documentação do projeto e visualizado via pgAdmin).*

---

##  Como Restaurar o Banco de Dados (Para a Equipe)

Se você precisar configurar o banco de dados no seu ambiente local através do backup fornecido (`.sql`), siga os passos abaixo no **pgAdmin 4**:

1. Abra o **pgAdmin 4** no seu computador.
2. Crie um novo banco de dados vazio com o nome `itassist_db`:
   * Clique com o botão direito em **Databases** > **Create** > **Database...**
   * Nome: `itassist_db` e clique em *Save*.
3. Restaure o arquivo de backup:
   * Clique com o botão direito em cima do novo banco de dados `itassist_db`.
   * Selecione **Restore...**
   * Em *Filename*, selecione o arquivo `.sql` de backup incluído no repositório.
   * Clique no botão **Restore**.

---

## 🚀 Tecnologias Utilizadas
* **Banco de Dados:** PostgreSQL
* **Ferramenta de Gestão:** pgAdmin 4
* **Controle de Versão:** Git & GitHub
